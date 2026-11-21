# SRS – Software Requirements Specification – LIÊN HOA KID 1.0

Cập nhật: 2026-11-21 · Hợp nhất Hồ sơ thiết kế v1.0 và Master Prompt. Mức ưu tiên: **P1** = bắt buộc cho bản dùng thật; **P2** = làm sau P1 nếu còn thời gian/ngân sách (vẫn nằm trong phạm vi, không bị loại).

## 1. Mâu thuẫn giữa hai tài liệu nguồn và cách xử lý
| Điểm | Hồ sơ v1.0 | Master Prompt | Xử lý trong SRS |
|---|---|---|---|
| Màn hình | 11 | 16 | Lấy 16 (hợp của hai bên) |
| Quản trị | 5 nhóm chính | 15 nhóm CRUD | Lấy 15, P1 cho nhóm nội dung và người dùng |
| Lộ trình | HSK chung | HSK 1–6 + nâng cao | Khung dữ liệu hỗ trợ HSK 1–6; nội dung nhập dần (P1: Làm quen, Cơ bản, HSK 1) |
| Ngân sách | 33 triệu | tối đa 35 triệu | Mục tiêu 33, trần 35 |
| Đăng ký học sinh | phụ huynh quản lý hồ sơ trẻ | cho phép cả hai | Học sinh tự đăng ký; phụ huynh xác nhận/liên kết; vẫn cho phụ huynh tạo hồ sơ cho trẻ nhỏ |

## 2. Yêu cầu chức năng
### FR-01 Tài khoản (P1)
Đăng ký, đăng nhập email/mật khẩu, đăng xuất, quên/đổi mật khẩu, xác thực email, quản lý phiên.
- **Đăng ký học sinh**: chọn nhóm tuổi/năm sinh, trình độ, mục tiêu; dưới ngưỡng tuổi thì nhập email phụ huynh để xin xác nhận (xem ERD, mục Luồng đăng ký).
- **AC:** tài khoản chưa xác thực email không vào được dữ liệu học; học sinh `pending_parent` không ghi được tiến độ.

### FR-02 Hồ sơ học viên (P1)
Tên hiển thị, avatar, nhóm tuổi, trình độ, mục tiêu, ngày bắt đầu, trạng thái. Phụ huynh quản lý nhiều hồ sơ.
- **AC:** học viên chỉ sửa được trường cho phép của hồ sơ mình; không sửa `xp_total`, `streak_days`, `status`.

### FR-03 Lộ trình (P1)
Khóa học → Cấp độ → Chương → Bài học → Bài tập → Kiểm tra, lấy từ database. Ghi nhận cấp độ hiện tại và trạng thái.
- **AC:** không có dữ liệu khóa học gắn cứng trong giao diện; nội dung `draft/archived` không hiển thị.

### FR-04 Từ vựng (P1)
Hán tự giản thể, Pinyin, thanh điệu, nghĩa tiếng Việt, từ loại, âm thanh, hình ảnh, ví dụ, cấp độ, chủ đề; tìm kiếm, lọc, đánh dấu ôn.

### FR-05 Bài học (P1)
Các loại: từ vựng, Pinyin, phát âm, mẫu câu, nghe, đọc, giao tiếp, chủ đề, kiểm tra cuối bài. Ghi giờ bắt đầu/hoàn thành, điểm, đúng/sai.
- **AC:** hoàn thành bài qua RPC `complete_lesson`; tải lại trang không mất kết quả.

### FR-06 Trò chơi 2D
| Game | Ưu tiên |
|---|---|
| Flashcard, Matching, Pinyin Challenge, Listening Quiz, Picture Quiz | P1 |
| Word Builder, Speed Quiz, Daily Challenge | P2 |
Yêu cầu chung: phản hồi đúng/sai, điểm, đồng hồ khi phù hợp, màn hình kết quả, chơi lại, lưu lịch sử, chọn độ khó, câu hỏi lấy từ database.
- **AC:** kết quả lưu qua RPC `submit_game_result`; máy chủ đối chiếu đáp án và tự tính điểm/XP; gửi điểm giả bị từ chối.

### FR-07 Ôn tập (P1)
Tự lưu từ đã học và từ sai; danh sách ôn hằng ngày; hộp Leitner (khoảng 1, 2, 4, 7, 15, 30 ngày); chế độ ôn nhanh; thống kê ghi nhớ.

### FR-08 XP và thành tích (P1)
XP, cấp độ, huy hiệu, chuỗi ngày, nhiệm vụ hằng ngày, thống kê cá nhân. Không bảng xếp hạng công khai.

### FR-09 Thống kê (P1)
Tổng bài/từ/thời gian, tỷ lệ hoàn thành, điểm trung bình, chuỗi ngày, tiến độ theo cấp độ, biểu đồ ngày/tuần/tháng. Dữ liệu lấy từ kết quả thật.

### FR-10 Phụ huynh (P1)
Xác nhận đồng ý, liên kết học viên, xem tiến độ/thời gian/bài hoàn thành/kết quả/từ cần ôn, đặt mục tiêu và nhắc học. Chỉ thấy học viên đã liên kết `active`.

### FR-11 Quản trị
15 nhóm theo Master Prompt mục IV-12. Mỗi nhóm: danh sách, tìm kiếm, lọc, thêm, sửa, xem chi tiết, ẩn/xuất bản, xóa có xác nhận, kiểm tra đầu vào.
- P1: tài khoản, học viên, phụ huynh, khóa học, cấp độ, chương, bài học, từ vựng, media, câu hỏi, nhật ký.
- P2: quản lý trò chơi, thành tích, thông báo, báo cáo nâng cao.

### FR-12 Thông báo và hỗ trợ (P1 cơ bản)
Thông báo trong ứng dụng, nhắc học/ôn tập, hướng dẫn, FAQ, gửi và quản lý yêu cầu hỗ trợ. Push notification: P2, kiểm thử riêng từng nền tảng (iOS hạn chế).

### FR-13 Trang chủ (P1)
Landing page, giới thiệu, đăng nhập/đăng ký, liên hệ.

## 3. Yêu cầu phi chức năng
- **Bảo mật:** RLS cho mọi bảng dữ liệu người dùng; kiểm tra quyền ở database; không để `service_role` ở frontend; mật khẩu do Supabase Auth xử lý; không lộ `is_correct` ra client.
- **Quyền riêng tư trẻ em:** thu thập tối thiểu; consent có ghi nhận; quy trình yêu cầu sửa/xóa; không quảng cáo hành vi; rà soát pháp lý trước phát hành.
- **Hiệu năng:** phân trang; tối ưu ảnh/âm thanh; không tải toàn bộ thư viện cùng lúc.
- **Khả dụng:** giao diện tiếng Việt, nút lớn, responsive, tối ưu điện thoại; PWA cài được.
- **Mở rộng:** thêm cấp độ HSK, bộ bài, game mới, ngôn ngữ giao diện mà không viết lại hệ thống.
- **Sao lưu:** có quy trình sao lưu/khôi phục tài liệu hóa; sao lưu tự động phụ thuộc gói Supabase trả phí.

## 4. Âm thanh phát âm
Bản 1.0 không dùng TTS trả phí. Phương án: file âm thanh ghi sẵn trong `media_assets` (ưu tiên), Web Speech API làm dự phòng (chất lượng tiếng Trung phụ thuộc thiết bị). Cần chốt nguồn âm thanh.

## 5. Tiêu chí nghiệm thu chung
Chỉ coi một chức năng là xong khi chạy được với dữ liệu thật trong database và có kiểm thử đã chạy, ghi kết quả vào `PROJECT_STATUS.md`. Các kịch bản bắt buộc nằm ở `docs/PERMISSIONS.md` (mục kịch bản RLS).
