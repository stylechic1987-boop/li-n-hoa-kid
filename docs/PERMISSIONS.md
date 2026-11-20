# Ma trận phân quyền – LIÊN HOA KID

Trạng thái: **CHỜ DUYỆT**. Mọi quyền được thực thi bằng RLS và RPC trên database, không chỉ ẩn nút trên giao diện.

Ký hiệu: R = đọc, C = tạo, U = sửa, D = xóa, own = chỉ dữ liệu của mình, linked = hồ sơ đã liên kết, pub = chỉ nội dung `published`, RPC = chỉ qua hàm máy chủ, – = không có quyền.

| Dữ liệu | SUPER_ADMIN | ADMIN | CONTENT_EDITOR | PARENT | LEARNER |
|---|---|---|---|---|---|
| `profiles` | RUD | R, U (không đổi quyền) | – | R/U own | R/U own |
| `user_roles` | CRUD | R; cấp/thu ADMIN: không; cấp PARENT/LEARNER/EDITOR: có | – | R own | R own |
| `learner_profiles` | CRUD | RU | – | CRUD owned/linked | R/U own (trường giới hạn) |
| `parent_learner_links`, `parental_consents` | CRUD | R | – | C/R own, thu hồi consent | R own |
| courses, levels, units, lessons | CRUD | CRUD | CRUD | R pub | R pub |
| vocabulary, media, examples | CRUD | CRUD | CRUD | R pub | R pub |
| quizzes, questions | CRUD | CRUD | CRUD | R pub | R pub (không thấy `is_correct`) |
| `question_options.is_correct` | RPC | RPC | R (để soạn) | – | – |
| enrollments | CRUD | R | – | C/R/U linked | C/R/U own |
| lesson_progress, vocabulary_progress, review_schedules | R | R | – | R linked | R own; **ghi: RPC** |
| game_sessions, game_answers | R | R | – | R linked | R own; **ghi: RPC** |
| XP, streak, user_achievements | R | R; chỉnh tay: ghi audit | – | R linked | R own; **không tự ghi** |
| achievements (danh mục) | CRUD | CRUD | CRUD | R | R |
| daily_goals | R | R | – | CRUD linked | R own |
| notifications | CRUD | CRUD | – | R/U (đã đọc) own | R/U own |
| support_requests | CRUD | CRUD (trả lời) | – | C/R own | C/R own |
| audit_logs | R | R | – | – | – |
| Trang quản trị | Có | Có | Chỉ khu nội dung | – | – |

## Quy tắc bắt buộc
1. Vai trò lưu ở `user_roles`; kiểm tra bằng `has_role(uid, role)` (`SECURITY DEFINER`, `search_path` cố định).
2. Không ai tự cấp vai trò quản trị cho mình. Chỉ SUPER_ADMIN cấp/thu ADMIN.
3. CONTENT_EDITOR không đọc dữ liệu cá nhân học viên và không sửa vai trò.
4. Client không có INSERT/UPDATE trên bảng kết quả; các RPC `submit_game_result`, `complete_lesson`, `record_review` tự tính điểm/XP từ đáp án đúng lưu trên server.
5. Mọi thao tác ADMIN/SUPER_ADMIN/EDITOR ghi `audit_logs` bằng trigger.
6. Khóa `service_role` chỉ dùng ở môi trường máy chủ, không vào frontend.
7. Nội dung `draft/archived` không hiện ra ở lộ trình học.

## Kịch bản RLS sẽ kiểm thử (pgTAP)
A không đọc được B; phụ huynh không đọc được trẻ chưa liên kết; học viên không gọi được thao tác quản trị; editor không sửa `user_roles`; client không tự tăng XP; nội dung ẩn không xuất hiện; `is_correct` không lộ qua API.
