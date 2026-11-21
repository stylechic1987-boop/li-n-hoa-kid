# ERD – LIÊN HOA KID (30 bảng, PostgreSQL / Supabase)

Trạng thái: **CHỜ DUYỆT**, chưa có migration.

## Nguyên tắc
- Khóa chính UUID (`gen_random_uuid()`); mọi bảng nghiệp vụ có `created_at`, `updated_at`.
- Nội dung có `status`: `draft | published | archived`.
- Nội dung học (courses → lessons) được đọc bởi mọi người dùng đã đăng nhập khi `published`.
- Dữ liệu kết quả (progress, game, XP) **chỉ ghi qua RPC `SECURITY DEFINER`**, client không INSERT/UPDATE trực tiếp.
- Quyền xác định bằng `user_roles` + hàm `has_role()`, không tin claim do client gửi.

## Quyết định cần duyệt
Đã chốt theo chỉ đạo ngày 2026-11-21: **học sinh tự đăng ký tài khoản**.
- **Q1 (chốt).** Mỗi học viên có tài khoản `auth.users` riêng. `learner_profiles.user_id` trỏ tới tài khoản đó. Phụ huynh vẫn có thể tạo hồ sơ cho trẻ nhỏ chưa tự đăng nhập: khi đó `user_id` rỗng và `owner_id` là phụ huynh; sau này trẻ có thể được cấp tài khoản và gán `user_id`.
- **Q2 (chốt).** `parent_learner_links` là cơ chế liên kết phụ huynh với học viên, gồm cả trường hợp học sinh đã đăng ký trước rồi mới mời phụ huynh. `status`: `pending` (đã mời/đã yêu cầu), `active` (đã xác nhận), `revoked`. Phụ huynh chỉ xem dữ liệu khi `active`.
- **Q3 (chốt hướng, ngưỡng tuổi còn mở).** `parental_consents` ghi phiên bản chính sách, thời điểm, phương thức, email phụ huynh. Học sinh dưới ngưỡng tuổi (tạm 16, **cần đối chiếu pháp luật VN**) đăng ký xong ở trạng thái `pending_parent`: được vào xem giới thiệu nhưng chưa lưu dữ liệu học cho đến khi phụ huynh xác nhận qua email. Từ ngưỡng tuổi trở lên tự đồng ý. Người lớn tự học: `owner_id = user_id`, `is_self = true`.

### Luồng đăng ký học sinh
1. Học sinh đăng ký email + mật khẩu (Supabase Auth, xác thực email).
2. Chọn nhóm tuổi / năm sinh, trình độ, mục tiêu.
3. Nếu dưới ngưỡng tuổi: nhập email phụ huynh → hệ thống tạo `parental_consents` (chờ) và `parent_learner_links` (`pending`) → gửi email xác nhận.
4. Phụ huynh xác nhận (đăng nhập hoặc tạo tài khoản PARENT) → consent `active`, link `active`, học sinh được kích hoạt đầy đủ.
5. Nếu quá hạn không xác nhận, hồ sơ giữ ở trạng thái chờ và bị xóa theo chính sách lưu giữ (thời hạn cần chốt).

## Sơ đồ quan hệ chính
```mermaid
erDiagram
  profiles ||--o{ user_roles : has
  profiles ||--o{ learner_profiles : owns
  profiles ||--|| user_settings : has
  profiles ||--o{ parent_learner_links : parent
  learner_profiles ||--o{ parent_learner_links : linked
  learner_profiles ||--o{ parental_consents : consent
  courses ||--o{ levels : has
  levels ||--o{ units : has
  units ||--o{ lessons : has
  lessons ||--o{ lesson_vocabulary : has
  vocabulary ||--o{ lesson_vocabulary : in
  vocabulary ||--o{ example_sentences : has
  vocabulary ||--o{ media_assets : uses
  lessons ||--o{ quizzes : has
  quizzes ||--o{ questions : has
  questions ||--o{ question_options : has
  learner_profiles ||--o{ enrollments : enrolls
  courses ||--o{ enrollments : in
  learner_profiles ||--o{ lesson_progress : tracks
  lessons ||--o{ lesson_progress : of
  learner_profiles ||--o{ learning_sessions : studies
  learner_profiles ||--o{ vocabulary_progress : knows
  vocabulary ||--o{ vocabulary_progress : of
  vocabulary_progress ||--o| review_schedules : scheduled
  learner_profiles ||--o{ game_sessions : plays
  game_sessions ||--o{ game_answers : has
  questions ||--o{ game_answers : answers
  learner_profiles ||--o{ user_achievements : earns
  achievements ||--o{ user_achievements : of
  learner_profiles ||--o{ daily_goals : sets
  profiles ||--o{ notifications : receives
  profiles ||--o{ support_requests : submits
  profiles ||--o{ audit_logs : acts
```

## Bảng và cột chính

### Tài khoản
| Bảng | Cột chính |
|---|---|
| `profiles` | id (= auth.users.id), display_name, phone?, created_at |
| `user_roles` | user_id, role (`SUPER_ADMIN/ADMIN/CONTENT_EDITOR/PARENT/LEARNER`), UNIQUE(user_id, role) |
| `learner_profiles` | id, user_id? → auth.users (UNIQUE), owner_id → profiles, display_name, avatar, age_group, birth_year?, level, goal, is_self, status (`pending_parent/active/suspended`), xp_total, streak_days, last_study_date |
| `parent_learner_links` | parent_id?, parent_email, learner_id, status (`pending/active/revoked`), UNIQUE(parent_email, learner_id) |
| `parental_consents` | learner_id, parent_email, parent_id?, policy_version, token_hash, requested_at, consented_at?, method, revoked_at? |
| `user_settings` | user_id, locale, sound_on, reminder_time |

### Học liệu
| Bảng | Cột chính |
|---|---|
| `courses` | slug, title, description, track (`intro/basic/conversation/hsk/topic`), status, sort_order |
| `levels` | course_id, code (ví dụ HSK1), title, sort_order, status |
| `units` | level_id, title, sort_order, status |
| `lessons` | unit_id, type (`vocab/pinyin/pronunciation/sentence/listening/reading/conversation/topic/test`), title, objective, sort_order, status |
| `vocabulary` | hanzi, pinyin, tone_marks, meaning_vi, pos, level_code, topic, status |
| `lesson_vocabulary` | lesson_id, vocabulary_id, sort_order |
| `media_assets` | kind (`image/audio`), storage_path, vocabulary_id?, lesson_id?, mime, size_bytes |
| `example_sentences` | vocabulary_id, hanzi, pinyin, meaning_vi, audio_asset_id? |

### Bài tập và trò chơi
| Bảng | Cột chính |
|---|---|
| `quizzes` | lesson_id, title, pass_score, status |
| `questions` | quiz_id?, vocabulary_id?, type, prompt, difficulty, status |
| `question_options` | question_id, text, is_correct (**ẩn với client**, chỉ RPC đọc) |
| `game_sessions` | learner_id, game_type (8 loại), difficulty, started_at, ended_at, score, correct_count, wrong_count, xp_awarded |
| `game_answers` | session_id, question_id, option_id, is_correct, time_ms |

### Tiến độ
| Bảng | Cột chính |
|---|---|
| `enrollments` | learner_id, course_id, current_level_id, status, UNIQUE(learner_id, course_id) |
| `lesson_progress` | learner_id, lesson_id, started_at, completed_at, score, correct, wrong, status |
| `learning_sessions` | learner_id, started_at, ended_at, duration_sec |
| `vocabulary_progress` | learner_id, vocabulary_id, box (hộp ôn 0–5), correct_streak, last_seen_at, UNIQUE(learner_id, vocabulary_id) |
| `review_schedules` | vocabulary_progress_id, due_at, interval_days |
| `achievements` | code, title, condition_type, threshold, icon |
| `user_achievements` | learner_id, achievement_id, earned_at |
| `daily_goals` | learner_id, goal_date, target_minutes, target_words, achieved |

### Quản trị
| Bảng | Cột chính |
|---|---|
| `notifications` | recipient_id, type, title, body, read_at |
| `support_requests` | user_id, subject, message, status, reply, replied_by |
| `audit_logs` | actor_id, action, table_name, record_id, diff (jsonb), at |

## Thuật toán ôn tập (bản 1.0)
Hộp Leitner đơn giản: đúng thì tăng `box`, sai thì về box 0 hoặc 1; `interval_days` theo bảng cố định (1, 2, 4, 7, 15, 30). Nâng cấp thuật toán sau khi có dữ liệu thực.

## Thay đổi so với danh sách 30 bảng gốc
Không thêm bớt bảng. Hai điểm làm rõ: `question_options.is_correct` không cho client đọc; `learner_profiles` mang `xp_total`, `streak_days` (chỉ RPC cập nhật).
