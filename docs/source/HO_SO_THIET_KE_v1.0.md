# HỒ SƠ THIẾT KẾ DỰ ÁN LIÊN HOA KID
**Phiên bản:** 1.0  
**Đơn vị chủ quản:** Liên Hoa Global Education  
**Tên sản phẩm:** LIÊN HOA KID  
**Lĩnh vực:** Công nghệ giáo dục – EdTech – Học tiếng Trung  
**Mô hình:** Nền tảng học tập độc lập (Standalone Learning Platform)

---

# PHẦN I. TỔNG QUAN DỰ ÁN

## 1. Mục tiêu dự án

Xây dựng LIÊN HOA KID thành nền tảng học tiếng Trung có tính tương tác cao, giúp người học tiếp cận tiếng Trung thông qua hình ảnh, âm thanh, trò chơi, bài tập và lộ trình học tập cá nhân.

Nền tảng hướng đến:
- Trẻ em mới bắt đầu học tiếng Trung.
- Học sinh trung học.
- Học sinh, sinh viên và người trưởng thành.
- Người học tiếng Trung từ cơ bản đến nâng cao.
- Phụ huynh có nhu cầu theo dõi quá trình học của con.

## 2. Định hướng sản phẩm

LIÊN HOA KID không chỉ là ứng dụng trò chơi học từ vựng. Sản phẩm cần có ba thành phần:

**A. Hệ thống học tập**
- Chương trình học theo cấp độ.
- Bài học từ vựng, Pinyin, chữ Hán và mẫu câu.
- Nghe, đọc, luyện tập, kiểm tra.
- Ôn tập thông minh dựa trên kết quả.

**B. Hệ thống trò chơi giáo dục**
- Ghép từ với hình ảnh.
- Ghép chữ Hán với Pinyin.
- Chọn đáp án đúng.
- Nghe âm thanh và chọn từ.
- Sắp xếp từ thành câu.
- Vượt thử thách theo cấp độ.

**C. Hệ thống quản lý học tập**
- Hồ sơ người học.
- Tiến độ học tập.
- Điểm số và thành tích.
- Lịch sử học.
- Nhắc học.
- Khu vực phụ huynh.
- Quản trị nội dung và người dùng.

## 3. Phạm vi sản phẩm

Sản phẩm được thiết kế cho mọi lứa tuổi, sử dụng hệ thống lộ trình thích ứng:

| Nhóm | Định hướng nội dung |
|---|---|
| 6–10 tuổi | Hình ảnh, âm thanh, từ vựng cơ bản, trò chơi |
| 11–14 tuổi | Từ vựng, mẫu câu, giao tiếp, bài tập |
| 15–18 tuổi | Ngữ pháp, hội thoại, luyện đọc và viết |
| Người trưởng thành | Giao tiếp, công việc, du lịch, HSK |
| Người học nâng cao | HSK, đọc hiểu, từ vựng chuyên sâu |

Người dùng có thể lựa chọn độ tuổi và trình độ đầu vào. Hệ thống không khóa nội dung chỉ theo tuổi mà còn căn cứ vào năng lực học tập.

---

# PHẦN II. BRD – BUSINESS REQUIREMENTS DOCUMENT

## 4. Bài toán kinh doanh

Các hình thức học truyền thống thường thiếu tính tương tác, khó duy trì thói quen học và chưa cung cấp đầy đủ dữ liệu để phụ huynh hoặc người học tự đánh giá tiến độ.

LIÊN HOA KID giải quyết các vấn đề:
1. Học từ vựng nhưng khó ghi nhớ lâu.
2. Thiếu môi trường luyện tập thường xuyên.
3. Thiếu cơ chế tạo động lực học.
4. Phụ huynh khó theo dõi tiến độ.
5. Khó cá nhân hóa nội dung theo trình độ.
6. Thiếu công cụ quản trị nội dung tập trung.

## 5. Mục tiêu nghiệp vụ

- Xây dựng thư viện học liệu tiếng Trung có cấu trúc.
- Tạo trải nghiệm học trực quan và dễ sử dụng.
- Tăng tần suất học tập thông qua trò chơi và thành tích.
- Theo dõi kết quả từng người học.
- Cho phép phụ huynh quản lý tài khoản trẻ em.
- Cho phép quản trị viên tạo và cập nhật bài học.
- Có khả năng mở rộng nội dung mà không phải viết lại hệ thống.

## 6. Nhóm người dùng

| Vai trò | Nhu cầu |
|---|---|
| Học viên | Học, chơi, luyện tập, xem tiến độ |
| Phụ huynh | Quản lý hồ sơ trẻ, xem báo cáo |
| Giáo viên/biên tập viên | Tạo bài học, câu hỏi, học liệu |
| Quản trị viên | Quản lý người dùng, nội dung, cấu hình |
| Quản lý hệ thống | Theo dõi hoạt động, báo cáo, phân quyền |

## 7. Chỉ số đánh giá hiệu quả

Các chỉ số mục tiêu ban đầu cần đo lường sau khi ra mắt:

- Tỷ lệ người dùng hoàn thành bài học đầu tiên.
- Số ngày học trung bình mỗi tuần.
- Tỷ lệ quay lại học sau 7 ngày.
- Tỷ lệ hoàn thành bài tập.
- Điểm trung bình theo cấp độ.
- Số từ vựng được ghi nhớ.
- Tỷ lệ người học duy trì chuỗi ngày học.
- Tỷ lệ phụ huynh truy cập báo cáo.

Các chỉ số này là KPI mục tiêu để theo dõi, không phải số liệu đã đạt được.

---

# PHẦN III. SRS – SOFTWARE REQUIREMENTS SPECIFICATION

## 8. Yêu cầu chức năng

### FR-01. Đăng ký và đăng nhập
- Đăng ký tài khoản.
- Đăng nhập bằng email và mật khẩu.
- Đăng xuất.
- Quên mật khẩu.
- Đổi mật khẩu.
- Xác thực tài khoản.
- Quản lý phiên đăng nhập.
- Hỗ trợ hồ sơ trẻ em được phụ huynh quản lý.

### FR-02. Hồ sơ người học
Mỗi người học có:
- Mã người dùng.
- Tên hiển thị.
- Ngày sinh hoặc nhóm tuổi.
- Ảnh đại diện.
- Trình độ tiếng Trung.
- Mục tiêu học tập.
- Ngày bắt đầu học.
- Trạng thái tài khoản.

Một tài khoản phụ huynh có thể quản lý nhiều hồ sơ trẻ em.

### FR-03. Chọn lộ trình học
Người học được chọn:
- Làm quen tiếng Trung.
- Tiếng Trung cơ bản.
- Tiếng Trung giao tiếp.
- Lộ trình theo HSK.
- Học theo chủ đề.
- Luyện tập theo năng lực.

Hệ thống cần ghi nhận cấp độ hiện tại và trạng thái hoàn thành.

### FR-04. Hệ thống bài học
Mỗi bài học có:
- Tên bài.
- Mục tiêu.
- Từ vựng.
- Chữ Hán.
- Pinyin.
- Nghĩa tiếng Việt.
- Âm thanh phát âm.
- Hình ảnh minh họa.
- Ví dụ và mẫu câu.
- Bài tập.
- Trạng thái hoàn thành.

### FR-05. Trò chơi học tập
Các trò chơi cốt lõi:

1. Flashcard: lật thẻ ghi nhớ.
2. Matching: nối chữ Hán với nghĩa.
3. Pinyin Challenge: ghép chữ với Pinyin.
4. Listening Quiz: nghe và chọn đáp án.
5. Picture Quiz: nhìn hình đoán từ.
6. Word Builder: sắp xếp từ thành câu.
7. Speed Quiz: trả lời trong thời gian giới hạn.
8. Daily Challenge: thử thách hàng ngày.

Mỗi lượt chơi cần lưu điểm, thời gian, số câu đúng, số câu sai và nội dung đã luyện tập.

### FR-06. Hệ thống ôn tập
- Ghi nhận từ vựng đã học.
- Ghi nhận từ vựng chưa nhớ.
- Tự đưa từ sai vào danh sách ôn tập.
- Tạo danh sách ôn tập hàng ngày.
- Lặp lại nội dung theo lịch ôn.
- Thống kê tỷ lệ ghi nhớ.

Giai đoạn đầu sử dụng thuật toán ôn tập theo khoảng thời gian đơn giản; có thể nâng cấp thuật toán sau khi có dữ liệu thực tế.

### FR-07. Thành tích và động lực
- Điểm kinh nghiệm XP.
- Huy hiệu.
- Chuỗi ngày học.
- Cấp độ người học.
- Nhiệm vụ hàng ngày.
- Thành tích hoàn thành bài học.
- Bảng thành tích cá nhân.

Không triển khai bảng xếp hạng công khai dành cho trẻ em trong phiên bản đầu.

### FR-08. Thống kê học tập
Hiển thị:
- Tổng thời gian học.
- Số bài đã hoàn thành.
- Số từ vựng đã học.
- Tỷ lệ trả lời đúng.
- Điểm kiểm tra.
- Lịch sử học tập.
- Tiến độ theo lộ trình.
- Nội dung cần ôn tập.

### FR-09. Khu vực phụ huynh
- Liên kết hồ sơ trẻ với phụ huynh.
- Xem tổng quan tiến độ.
- Xem thời gian học.
- Xem bài đã hoàn thành.
- Xem kết quả kiểm tra.
- Xem từ vựng cần ôn.
- Thiết lập mục tiêu học.
- Thiết lập nhắc học.
- Quản lý hồ sơ trẻ.

### FR-10. Quản trị nội dung
Quản trị viên được phép:
- Tạo khóa học.
- Tạo cấp độ.
- Tạo chủ đề.
- Tạo bài học.
- Tạo từ vựng.
- Tạo câu hỏi.
- Tải hình ảnh và âm thanh.
- Sắp xếp thứ tự bài học.
- Xuất bản hoặc ẩn nội dung.
- Xem lịch sử chỉnh sửa.

### FR-11. Thông báo
- Nhắc học hàng ngày.
- Nhắc bài chưa hoàn thành.
- Nhắc ôn tập.
- Thông báo thành tích.
- Thông báo dành cho phụ huynh.

Phiên bản đầu có thể dùng thông báo trong ứng dụng và nhắc lịch qua giao diện. Push notification cần được kiểm thử theo từng nền tảng.

### FR-12. Hỗ trợ
- Hướng dẫn sử dụng.
- Câu hỏi thường gặp.
- Biểu mẫu gửi yêu cầu hỗ trợ.
- Thông tin liên hệ Liên Hoa.

## 9. Yêu cầu phi chức năng

### Hiệu năng
- Giao diện tải nhanh trên mạng phổ thông.
- Tối ưu hình ảnh và âm thanh.
- Phân trang danh sách dữ liệu.
- Tránh tải toàn bộ thư viện học liệu cùng lúc.

### Bảo mật
- Mật khẩu phải được xử lý bởi hệ thống xác thực an toàn.
- Không lưu mật khẩu dạng văn bản.
- Kiểm tra quyền truy cập phía máy chủ.
- Người học không được truy cập dữ liệu của người khác.
- Phụ huynh chỉ xem được hồ sơ trẻ đã liên kết.
- Quản trị viên có phân quyền theo vai trò.
- Không đưa khóa bí mật quản trị vào mã nguồn frontend.

### Khả năng sử dụng
- Giao diện tiếng Việt.
- Chữ dễ đọc.
- Nút bấm lớn, rõ ràng.
- Điều hướng đơn giản.
- Thiết kế responsive.
- Tối ưu cho màn hình điện thoại.

### Khả năng mở rộng
- Thêm cấp độ HSK.
- Thêm ngôn ngữ giao diện.
- Thêm bộ bài học.
- Thêm trò chơi mới.
- Thêm chức năng học trực tiếp.
- Mở rộng dung lượng lưu trữ.

### Quyền riêng tư trẻ em
- Có cơ chế xác nhận và đồng ý của phụ huynh khi cần.
- Thu thập dữ liệu tối thiểu.
- Không hiển thị thông tin cá nhân trẻ công khai.
- Có cơ chế yêu cầu chỉnh sửa hoặc xóa dữ liệu.
- Không dùng quảng cáo hành vi hướng đến trẻ em.
- Xây dựng quy định xử lý dữ liệu cá nhân phù hợp pháp luật hiện hành.

---

# PHẦN IV. KIẾN TRÚC HỆ THỐNG

## 10. Kiến trúc tổng thể

LIÊN HOA KID được triển khai độc lập, không kết nối CRM Liên Hoa, không đồng bộ dữ liệu với các hệ thống tuyển sinh hoặc nền tảng kinh doanh khác trong phạm vi phiên bản này.

Kiến trúc đề xuất:

**Tầng 1 – Giao diện**
- Web application.
- Progressive Web App (PWA).
- Responsive trên điện thoại, máy tính bảng, máy tính.
- Giao diện 2D.

**Tầng 2 – Ứng dụng**
- Đăng nhập và xác thực.
- Quản lý hồ sơ.
- Quản lý bài học.
- Trò chơi.
- Ôn tập.
- Thống kê.
- Phụ huynh.
- Quản trị.

**Tầng 3 – Dữ liệu**
- PostgreSQL.
- Lưu trữ ảnh và âm thanh.
- Phân quyền truy cập.
- Sao lưu dữ liệu.

**Tầng 4 – Dịch vụ**
- Xác thực.
- Lưu trữ.
- API.
- Nhật ký hoạt động.
- Thông báo.

## 11. Công nghệ đề xuất

| Thành phần | Công nghệ |
|---|---|
| Frontend | React + TypeScript |
| Giao diện | CSS responsive / Tailwind CSS |
| Game 2D | HTML5 Canvas hoặc React component |
| Backend | Supabase |
| Database | PostgreSQL |
| Authentication | Supabase Auth |
| File storage | Supabase Storage |
| Hosting | Static hosting |
| PWA | Web App Manifest + Service Worker |
| Kiểm thử | Vitest / Playwright |

**Lưu ý:** PWA giúp dùng ứng dụng trên nhiều thiết bị mà không phải phát triển đồng thời ba ứng dụng native. Phiên bản đầu chưa bao gồm ứng dụng native độc lập trên App Store và Google Play.

## 12. Sơ đồ kiến trúc

```text
                 LIÊN HOA KID
                       |
          +------------+------------+
          |                         |
      HỌC VIÊN                  PHỤ HUYNH
          |                         |
          +------------+------------+
                       |
                 FRONTEND
              React + TypeScript
                       |
                 APPLICATION
          +------------+------------+
          |            |            |
       Learning       Game       Dashboard
          |            |            |
          +------------+------------+
                       |
                    API
                       |
                  SUPABASE
          +------------+------------+
          |            |            |
       Auth         Database       Storage
          |            |            |
          +------------+------------+
                       |
                 ADMIN PORTAL
```

## 13. Nguyên tắc vận hành dữ liệu

- Mỗi học viên có một mã định danh.
- Mỗi bài học có một mã định danh.
- Mỗi lần làm bài tạo một bản ghi kết quả.
- Tiến độ học được tổng hợp từ dữ liệu hoạt động.
- Điểm và XP phải được tính ở phía máy chủ hoặc thông qua cơ chế kiểm soát tin cậy.
- Không cho frontend tự ý cập nhật điểm tổng hoặc quyền quản trị.
- Tách dữ liệu hồ sơ, nội dung học và kết quả học.

---

# PHẦN V. KIẾN TRÚC CƠ SỞ DỮ LIỆU

## 14. Danh sách bảng dữ liệu

### Nhóm tài khoản
1. `profiles` – hồ sơ tài khoản.
2. `user_roles` – vai trò người dùng.
3. `learner_profiles` – hồ sơ học viên.
4. `parent_learner_links` – liên kết phụ huynh và trẻ.
5. `user_settings` – cài đặt cá nhân.

### Nhóm học liệu
6. `courses` – khóa học.
7. `levels` – cấp độ.
8. `units` – chương học.
9. `lessons` – bài học.
10. `vocabulary` – từ vựng.
11. `lesson_vocabulary` – từ vựng trong bài.
12. `media_assets` – hình ảnh và âm thanh.
13. `example_sentences` – câu ví dụ.

### Nhóm bài tập
14. `quizzes` – bài kiểm tra.
15. `questions` – câu hỏi.
16. `question_options` – lựa chọn đáp án.
17. `game_sessions` – phiên chơi.
18. `game_answers` – câu trả lời trong trò chơi.

### Nhóm tiến độ
19. `enrollments` – đăng ký lộ trình.
20. `lesson_progress` – tiến độ bài học.
21. `learning_sessions` – phiên học.
22. `vocabulary_progress` – tiến độ từ vựng.
23. `review_schedules` – lịch ôn tập.
24. `achievements` – danh mục thành tích.
25. `user_achievements` – thành tích của học viên.
26. `daily_goals` – mục tiêu hàng ngày.

### Nhóm quản trị
27. `notifications` – thông báo.
28. `support_requests` – yêu cầu hỗ trợ.
29. `audit_logs` – nhật ký quản trị.
30. `parental_consents` – ghi nhận sự đồng ý của phụ huynh.

## 15. Quan hệ dữ liệu chính

```text
profiles
  |
  +---- learner_profiles
  |          |
  |          +---- enrollments
  |          |        |
  |          |        +---- courses
  |          |
  |          +---- lesson_progress
  |          |
  |          +---- learning_sessions
  |          |
  |          +---- vocabulary_progress
  |          |
  |          +---- game_sessions
  |
  +---- parent_learner_links
  |
  +---- user_roles

courses
  |
  +---- levels
           |
           +---- units
                    |
                    +---- lessons
                             |
                             +---- lesson_vocabulary
                             +---- quizzes
                             +---- media_assets
```

## 16. Nguyên tắc thiết kế dữ liệu

- Sử dụng UUID làm khóa chính.
- Có `created_at`, `updated_at` cho các bảng nghiệp vụ.
- Có trạng thái `draft`, `published`, `archived` đối với nội dung.
- Có khóa ngoại để bảo đảm tính toàn vẹn.
- Có chỉ mục cho các trường thường xuyên truy vấn.
- Dùng Row Level Security (RLS) cho dữ liệu người dùng.
- Tách dữ liệu quản trị khỏi dữ liệu học viên.
- Không lưu thông tin nhạy cảm không cần thiết.

---

# PHẦN VI. THIẾT KẾ GIAO DIỆN 2D

## 17. Định hướng mỹ thuật

Phong cách:
- 2D thân thiện.
- Màu sắc tươi sáng.
- Hình minh họa hoạt hình.
- Biểu tượng trực quan.
- Chuyển động nhẹ.
- Không sử dụng đồ họa 3D.

Màu nhận diện đề xuất:
- Đỏ Liên Hoa: màu nhấn.
- Vàng: thành tích và phần thưởng.
- Trắng: nền chính.
- Xanh lá: hoàn thành.
- Xanh dương: nội dung học tập.

## 18. Danh sách màn hình

### Màn hình 01 – Đăng nhập
- Logo Liên Hoa Kid.
- Email.
- Mật khẩu.
- Đăng nhập.
- Đăng ký.
- Quên mật khẩu.

### Màn hình 02 – Chọn hồ sơ
- Danh sách hồ sơ học viên.
- Tạo hồ sơ mới.
- Chọn avatar.
- Chọn nhóm tuổi.
- Chọn trình độ.

### Màn hình 03 – Trang chủ
- Lời chào.
- Avatar.
- Tiến độ học.
- Bài học tiếp theo.
- Thử thách hôm nay.
- Từ vựng cần ôn.
- Thành tích.

### Màn hình 04 – Lộ trình học
- Danh sách khóa học.
- Cấp độ.
- Chương học.
- Bài học.
- Trạng thái hoàn thành.

### Màn hình 05 – Chi tiết bài học
- Chữ Hán.
- Pinyin.
- Nghĩa tiếng Việt.
- Hình minh họa.
- Nút nghe phát âm.
- Ví dụ.
- Nút tiếp tục.

### Màn hình 06 – Trò chơi
- Chọn trò chơi.
- Hiển thị câu hỏi.
- Đáp án.
- Điểm.
- Kết quả.
- Nút chơi lại.

### Màn hình 07 – Ôn tập
- Danh sách từ cần ôn.
- Phát âm.
- Thẻ ghi nhớ.
- Kết quả ghi nhớ.

### Màn hình 08 – Thành tích
- XP.
- Huy hiệu.
- Chuỗi ngày học.
- Tổng số bài hoàn thành.

### Màn hình 09 – Thống kê
- Biểu đồ thời gian học.
- Tỷ lệ hoàn thành.
- Kết quả bài kiểm tra.
- Từ vựng đã học.

### Màn hình 10 – Phụ huynh
- Danh sách hồ sơ trẻ.
- Tiến độ từng trẻ.
- Thời gian học.
- Báo cáo theo tuần.
- Cài đặt mục tiêu.

### Màn hình 11 – Quản trị
- Dashboard.
- Quản lý người dùng.
- Quản lý khóa học.
- Quản lý bài học.
- Quản lý từ vựng.
- Quản lý câu hỏi.
- Quản lý hình ảnh và âm thanh.
- Báo cáo.

## 19. Điều hướng chính

Thanh điều hướng học viên:

- Trang chủ.
- Học tập.
- Trò chơi.
- Ôn tập.
- Thành tích.
- Cá nhân.

Khu vực phụ huynh và quản trị có điều hướng riêng, không dùng chung quyền truy cập với học viên.

---

# PHẦN VII. KẾ HOẠCH TRIỂN KHAI

## 20. Các giai đoạn thực hiện

### Giai đoạn 1 – Phân tích và thiết kế
Thời gian: Tuần 1

- Chốt chức năng.
- Hoàn thiện luồng người dùng.
- Thiết kế cơ sở dữ liệu.
- Thiết kế giao diện.
- Xây dựng tiêu chí nghiệm thu.

**Đầu ra:** BRD, SRS, ERD, UI flow, thiết kế giao diện.

### Giai đoạn 2 – Nền tảng hệ thống
Thời gian: Tuần 2

- Khởi tạo dự án.
- Xây dựng cấu trúc frontend.
- Cấu hình Supabase.
- Xác thực.
- Phân quyền.
- Hồ sơ học viên.
- Khu vực phụ huynh cơ bản.

**Đầu ra:** Hệ thống đăng nhập và hồ sơ hoạt động.

### Giai đoạn 3 – Hệ thống học tập
Thời gian: Tuần 3–4

- Khóa học.
- Cấp độ.
- Bài học.
- Từ vựng.
- Pinyin.
- Âm thanh.
- Hình ảnh.
- Tiến độ học.

**Đầu ra:** Có thể học một lộ trình từ đầu đến cuối.

### Giai đoạn 4 – Trò chơi và ôn tập
Thời gian: Tuần 5–6

- Flashcard.
- Matching.
- Quiz.
- Listening.
- Word Builder.
- Lưu điểm.
- Lịch sử chơi.
- Ôn tập từ vựng.

**Đầu ra:** Hoàn thiện vòng lặp học – luyện tập – ôn tập.

### Giai đoạn 5 – Phụ huynh và quản trị
Thời gian: Tuần 7

- Báo cáo phụ huynh.
- Quản lý học viên.
- Quản lý nội dung.
- Quản lý câu hỏi.
- Thống kê quản trị.

**Đầu ra:** Có thể vận hành nội dung và theo dõi người học.

### Giai đoạn 6 – Kiểm thử và phát hành
Thời gian: Tuần 8

- Kiểm thử chức năng.
- Kiểm thử phân quyền.
- Kiểm thử dữ liệu.
- Kiểm thử đa thiết bị.
- Tối ưu hiệu năng.
- Kiểm tra bảo mật.
- Hướng dẫn quản trị.
- Phát hành PWA.

**Đầu ra:** Phiên bản LIÊN HOA KID 1.0.

---

# PHẦN VIII. DỰ TOÁN NGÂN SÁCH

## 21. Phân bổ ngân sách dự kiến

| Hạng mục | Ngân sách |
|---|---:|
| Phân tích nghiệp vụ, kiến trúc | 2.000.000 |
| Thiết kế UI/UX 2D | 3.500.000 |
| Frontend và responsive/PWA | 6.500.000 |
| Backend, database, authentication | 5.000.000 |
| Hệ thống bài học và học liệu | 4.000.000 |
| Trò chơi và ôn tập | 4.000.000 |
| Phụ huynh và quản trị | 3.000.000 |
| Kiểm thử, bảo mật, triển khai | 2.000.000 |
| Dự phòng hạ tầng và phát sinh | 3.000.000 |
| **TỔNG CỘNG** | **33.000.000 VNĐ** |

Ngân sách trên là dự toán mục tiêu, cần xác nhận theo nhân sự, khối lượng học liệu, hạ tầng và báo giá thực tế.

## 22. Giới hạn ngân sách

Để duy trì mức dưới 35 triệu đồng:
- Ưu tiên PWA thay vì ba ứng dụng native.
- Sử dụng thư viện giao diện và công cụ mã nguồn mở.
- Dùng một backend và một cơ sở dữ liệu.
- Dùng hình minh họa 2D tối ưu dung lượng.
- Không triển khai AI hội thoại hoặc chấm phát âm AI trong bản 1.0.
- Không xây dựng hệ thống livestream.
- Không triển khai thanh toán trực tuyến phức tạp.
- Không tích hợp CRM hoặc hệ thống tuyển sinh.

Chi phí duy trì máy chủ, tên miền, nội dung âm thanh, hỗ trợ kỹ thuật và nhân sự vận hành sau phát hành cần được theo dõi riêng.

---

# PHẦN IX. KIỂM THỬ VÀ NGHIỆM THU

## 23. Tiêu chí nghiệm thu

### Nhóm tài khoản
- Đăng ký, đăng nhập, đăng xuất hoạt động.
- Quên mật khẩu hoạt động.
- Phân quyền đúng vai trò.
- Phụ huynh liên kết đúng hồ sơ trẻ.

### Nhóm học tập
- Bài học hiển thị đúng.
- Pinyin và nghĩa tiếng Việt chính xác.
- Âm thanh phát được.
- Tiến độ được lưu sau khi học.
- Không mất kết quả khi tải lại trang.

### Nhóm trò chơi
- Câu hỏi và đáp án đúng.
- Điểm số được ghi nhận.
- Kết quả được lưu.
- Không thể tự sửa điểm bằng frontend.

### Nhóm phụ huynh
- Chỉ xem được hồ sơ đã liên kết.
- Báo cáo khớp dữ liệu học tập.
- Không truy cập được dữ liệu người khác.

### Nhóm quản trị
- Tạo, sửa, ẩn bài học.
- Quản lý từ vựng.
- Quản lý câu hỏi.
- Nội dung đã xuất bản hiển thị đúng.

### Nhóm đa thiết bị
- Hoạt động trên desktop.
- Hoạt động trên Android.
- Hoạt động trên iOS qua trình duyệt/PWA.
- Responsive trên máy tính bảng.

### Nhóm bảo mật
- RLS được bật và kiểm thử.
- Không lộ khóa bí mật.
- Không truy cập chéo hồ sơ.
- Có chính sách sao lưu và phục hồi.

---

# PHẦN X. QUẢN TRỊ VÀ VẬN HÀNH

## 24. Quy trình quản trị nội dung

1. Biên tập viên tạo khóa học.
2. Quản trị viên tạo cấp độ và chương.
3. Biên tập viên tạo bài học.
4. Nhập từ vựng, Pinyin, nghĩa, ví dụ.
5. Tải âm thanh và hình ảnh.
6. Tạo câu hỏi và đáp án.
7. Kiểm tra nội dung.
8. Xuất bản.
9. Học viên truy cập.
10. Hệ thống ghi nhận kết quả.

## 25. Sao lưu và an toàn dữ liệu

- Sao lưu cơ sở dữ liệu định kỳ.
- Có quy trình khôi phục.
- Lưu lịch sử thay đổi nội dung.
- Hạn chế quyền quản trị.
- Kiểm tra log truy cập.
- Không sửa trực tiếp dữ liệu sản xuất nếu không có quy trình kiểm soát.

---

# PHẦN XI. ĐỊNH HƯỚNG PHÁT TRIỂN SAU PHIÊN BẢN 1.0

Các chức năng sau không nằm trong cam kết ngân sách bản đầu:

1. AI luyện nói và đánh giá phát âm.
2. AI trợ giảng tiếng Trung.
3. Lớp học trực tuyến với giáo viên.
4. Ứng dụng Android native.
5. Ứng dụng iOS native.
6. Hệ thống chứng chỉ và thi thử HSK nâng cao.
7. Gói thành viên và thanh toán.
8. Thư viện video bài giảng lớn.
9. Hệ thống cộng đồng học tập.
10. Tích hợp CRM Liên Hoa trong một dự án riêng, chỉ khi có quyết định thay đổi phạm vi.

---

# PHẦN XII. KẾT LUẬN VÀ ĐỊNH NGHĨA SẢN PHẨM

LIÊN HOA KID 1.0 được định nghĩa là nền tảng học tiếng Trung độc lập, giao diện 2D, hoạt động trên nhiều loại thiết bị thông qua PWA.

Sản phẩm bao gồm:
- Hệ thống tài khoản.
- Hồ sơ học viên.
- Lộ trình học.
- Thư viện bài học.
- Từ vựng, Pinyin, âm thanh.
- Trò chơi giáo dục.
- Ôn tập.
- Thành tích.
- Thống kê.
- Khu vực phụ huynh.
- Quản trị nội dung.
- Phân quyền và bảo mật.

**Ngân sách mục tiêu: 33.000.000 VNĐ.**  
**Thời gian mục tiêu: 8 tuần.**  
**Phạm vi: Phiên bản 1.0 có thể đưa vào sử dụng thực tế, với điều kiện hoàn thành kiểm thử và nghiệm thu.**

Đây là cơ sở để chuyển sang thiết kế UI/UX chi tiết, triển khai database, phát triển frontend/backend và kiểm thử hệ thống.