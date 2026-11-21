# BRD – Business Requirements Document – LIÊN HOA KID 1.0

Mã dự án: LHK-2026-001 · Đơn vị chủ quản: Liên Hoa Global Education · Cập nhật: 2026-11-21

## 1. Mục tiêu
Xây dựng nền tảng học tiếng Trung độc lập (web + PWA, giao diện 2D) cho trẻ em, học sinh, sinh viên và người trưởng thành, kết hợp bài học, trò chơi, ôn tập thông minh, theo dõi tiến độ và khu vực phụ huynh.

## 2. Bài toán kinh doanh
1. Người học khó ghi nhớ từ vựng lâu dài.
2. Thiếu môi trường luyện tập đều đặn và động lực học.
3. Phụ huynh khó theo dõi tiến độ của con.
4. Khó cá nhân hóa theo trình độ.
5. Chưa có công cụ tập trung để quản trị học liệu.

## 3. Phạm vi
**Trong phạm vi 1.0:** tài khoản (học sinh tự đăng ký), hồ sơ học viên, lộ trình, bài học, từ vựng, 8 trò chơi 2D, ôn tập, XP/huy hiệu/chuỗi ngày, thống kê, khu vực phụ huynh, quản trị nội dung và người dùng, thông báo trong ứng dụng, hỗ trợ, PWA.

**Ngoài phạm vi 1.0:** kết nối CRM Liên Hoa, thanh toán, AI luyện nói/chấm phát âm, livestream, ứng dụng native, bảng xếp hạng công khai cho trẻ em, quảng cáo hành vi.

## 4. Các bên liên quan
| Vai trò | Nhu cầu chính |
|---|---|
| Học viên (LEARNER) | Tự đăng ký, học, chơi, ôn tập, xem tiến độ |
| Phụ huynh (PARENT) | Xác nhận đồng ý, theo dõi và đặt mục tiêu cho con |
| Biên tập viên (CONTENT_EDITOR) | Soạn bài, từ vựng, câu hỏi, học liệu |
| Quản trị viên (ADMIN) | Quản lý người dùng, nội dung, báo cáo, hỗ trợ |
| Quản trị tối cao (SUPER_ADMIN) | Phân quyền, cấu hình, nhật ký |

## 4b. Ràng buộc
- Ngân sách tối đa 35.000.000 VNĐ; thời gian mục tiêu 8 tuần.
- Ưu tiên mã nguồn mở và hạ tầng miễn phí/chi phí thấp; không dùng API trả phí khi chưa được duyệt.
- Dữ liệu trẻ em: phải tuân thủ pháp luật Việt Nam hiện hành về dữ liệu cá nhân (cần rà soát trước phát hành).

## 5. Mục tiêu nghiệp vụ và KPI mục tiêu
Các chỉ số dưới đây là mục tiêu để đo sau khi ra mắt, chưa phải số liệu đã đạt được.
| Chỉ số | Cách đo |
|---|---|
| Hoàn thành bài học đầu tiên | % học viên mới hoàn thành ≥1 bài |
| Quay lại sau 7 ngày | % học viên có phiên học ở ngày 7–8 |
| Ngày học trung bình mỗi tuần | từ `learning_sessions` |
| Duy trì chuỗi ngày | % có `streak_days` ≥ 3 |
| Tỷ lệ hoàn thành bài tập | bài hoàn thành / bài bắt đầu |
| Từ vựng ghi nhớ | số từ ở hộp ôn ≥ 3 |
| Phụ huynh xem báo cáo | % phụ huynh có lượt xem trong tuần |
Ngưỡng mục tiêu cụ thể do chủ dự án đặt sau khi có số liệu nền.

## 6. Quy tắc nghiệp vụ chính
- BR-01. Học sinh tự đăng ký; dưới ngưỡng tuổi quy định thì cần phụ huynh xác nhận trước khi lưu dữ liệu học.
- BR-02. Phụ huynh chỉ xem được học viên đã liên kết và đã xác nhận.
- BR-03. XP, điểm và chuỗi ngày chỉ do máy chủ tính; học viên không tự sửa được.
- BR-04. Nội dung ở trạng thái `draft/archived` không hiện trong lộ trình học.
- BR-05. Không công khai thông tin cá nhân của trẻ; không bảng xếp hạng công khai.
- BR-06. Mọi thao tác quản trị được ghi `audit_logs`.
- BR-07. Người dùng có quyền yêu cầu chỉnh sửa hoặc xóa dữ liệu cá nhân.

## 7. Rủi ro kinh doanh
1. Phạm vi full so với 8 tuần và 35 triệu: cần ưu tiên theo SRS (mức P1/P2).
2. Học liệu HSK 1–6 và âm thanh: chưa có nguồn, cần xác minh bản quyền.
3. Tuân thủ pháp luật dữ liệu trẻ em: cần tư vấn pháp lý trước phát hành.
4. Chi phí vận hành sau phát hành (Supabase gói trả phí, tên miền, hỗ trợ) chưa nằm trong ngân sách phát triển.
