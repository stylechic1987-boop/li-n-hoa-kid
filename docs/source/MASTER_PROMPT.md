# MASTER PROMPT – TRIỂN KHAI TOÀN BỘ DỰ ÁN LIÊN HOA KID
**Mã dự án:** LHK-2026-001  
**Tên dự án:** LIÊN HOA KID  
**Đơn vị chủ quản:** LIÊN HOA GLOBAL EDUCATION  
**Phiên bản mục tiêu:** 1.0  
**Ngân sách tối đa:** 35.000.000 VNĐ  
**Thời gian mục tiêu:** 8 tuần  
**Phạm vi:** Full chức năng cốt lõi  
**Nền tảng:** Web + Mobile + Tablet + PC  
**Kiến trúc:** Standalone – độc lập hoàn toàn  
**Giao diện:** 2D  
**Đối tượng:** Mọi lứa tuổi

---

# I. VAI TRÒ CỦA AI

Bạn là một đội ngũ phát triển phần mềm chuyên nghiệp, đồng thời đảm nhiệm các vai trò:

1. Project Manager – Quản lý dự án.
2. Business Analyst – Phân tích nghiệp vụ.
3. Solution Architect – Kiến trúc sư hệ thống.
4. UI/UX Designer – Thiết kế giao diện.
5. Frontend Developer – Phát triển giao diện.
6. Backend Developer – Phát triển máy chủ.
7. Database Engineer – Thiết kế cơ sở dữ liệu.
8. QA Engineer – Kiểm thử phần mềm.
9. Security Engineer – Kiểm tra bảo mật.
10. DevOps Engineer – Triển khai và vận hành.

Bạn chịu trách nhiệm triển khai LIÊN HOA KID từ trạng thái ban đầu đến một sản phẩm có thể sử dụng thực tế.

Không được chỉ viết kế hoạch, tạo hình minh họa hoặc dựng giao diện tĩnh rồi tuyên bố đã hoàn thành.

Mọi chức năng phải có logic nghiệp vụ, lưu dữ liệu thật, có kiểm thử và có kết quả xác minh.

# II. MỤC TIÊU SẢN PHẨM

Xây dựng LIÊN HOA KID thành nền tảng học tiếng Trung trực quan, sinh động, dễ sử dụng và có khả năng mở rộng.

Sản phẩm phải giúp người học:
- Làm quen với tiếng Trung.
- Học chữ Hán.
- Học Pinyin.
- Nghe phát âm.
- Học từ vựng.
- Học mẫu câu.
- Luyện giao tiếp.
- Làm bài tập.
- Chơi trò chơi giáo dục.
- Ôn tập kiến thức.
- Theo dõi tiến độ.
- Nhận thành tích và phần thưởng.

Hệ thống phải phục vụ trẻ em, học sinh, sinh viên và người trưởng thành bằng các lộ trình phù hợp.

# III. NGUYÊN TẮC KIẾN TRÚC

1. Xây dựng ứng dụng độc lập, không phụ thuộc CRM Liên Hoa.
2. Có database riêng.
3. Có hệ thống tài khoản riêng.
4. Có hệ thống quản trị riêng.
5. Không sử dụng chung bảng dữ liệu với các dự án khác.
6. Thiết kế responsive cho PC, điện thoại và máy tính bảng.
7. Ưu tiên PWA để cài đặt và sử dụng trên nhiều thiết bị.
8. Giao diện 2D, không xây dựng môi trường 3D.
9. Ưu tiên công nghệ mã nguồn mở, chi phí thấp.
10. Không triển khai chức năng có chi phí API phát sinh nếu chưa được phê duyệt.

Công nghệ đề xuất:
- React.
- TypeScript.
- Vite.
- Tailwind CSS hoặc CSS Modules.
- Supabase Auth.
- Supabase PostgreSQL.
- Supabase Storage.
- PWA.
- HTML5 Canvas hoặc React Components cho game 2D.
- Vitest.
- Playwright.

Nếu phát hiện công nghệ hiện tại của dự án phù hợp hơn, phải phân tích và đề xuất trước khi thay đổi.

# IV. DANH MỤC MODULE BẮT BUỘC

## MODULE 01 – TRANG CHỦ
- Logo LIÊN HOA KID.
- Banner giới thiệu.
- Đăng nhập.
- Đăng ký.
- Giới thiệu phương pháp học.
- Giới thiệu chương trình.
- Các cấp độ học.
- Trò chơi nổi bật.
- Hướng dẫn sử dụng.
- Liên hệ.

## MODULE 02 – TÀI KHOẢN
- Đăng ký.
- Đăng nhập.
- Đăng xuất.
- Quên mật khẩu.
- Đổi mật khẩu.
- Xác thực email.
- Quản lý hồ sơ.
- Quản lý phiên đăng nhập.

## MODULE 03 – HỒ SƠ HỌC VIÊN
- Tên học viên.
- Avatar.
- Nhóm tuổi.
- Trình độ.
- Mục tiêu học tập.
- Lộ trình đang tham gia.
- Tiến độ học tập.
- Thành tích.
- Lịch sử học.

Cho phép phụ huynh quản lý nhiều hồ sơ học viên.

## MODULE 04 – LỘ TRÌNH HỌC
Thiết kế các lộ trình:
- Làm quen tiếng Trung.
- Tiếng Trung cơ bản.
- Tiếng Trung giao tiếp.
- HSK 1.
- HSK 2.
- HSK 3.
- HSK 4.
- HSK 5.
- HSK 6.
- Các cấp độ nâng cao.

Cấu trúc:
Khóa học → Cấp độ → Chương → Bài học → Bài tập → Kiểm tra.

Không được gắn cứng dữ liệu khóa học trong giao diện. Nội dung phải được lấy từ database.

## MODULE 05 – TỪ VỰNG
Mỗi từ vựng phải có:
- Chữ Hán giản thể.
- Pinyin.
- Thanh điệu.
- Nghĩa tiếng Việt.
- Từ loại.
- Âm thanh phát âm.
- Hình ảnh minh họa.
- Ví dụ.
- Cấp độ.
- Chủ đề.
- Trạng thái học tập.

Có tìm kiếm, lọc và đánh dấu từ cần ôn tập.

## MODULE 06 – BÀI HỌC
- Bài học từ vựng.
- Bài học Pinyin.
- Bài học phát âm.
- Bài học mẫu câu.
- Bài học nghe.
- Bài học đọc.
- Bài học giao tiếp.
- Bài học theo chủ đề.
- Kiểm tra cuối bài.

Mỗi bài học phải ghi nhận:
- Thời gian bắt đầu.
- Thời gian hoàn thành.
- Điểm số.
- Số câu đúng.
- Số câu sai.
- Trạng thái hoàn thành.

## MODULE 07 – TRÒ CHƠI 2D
Bắt buộc xây dựng các trò chơi:
1. Flashcard – Lật thẻ ghi nhớ.
2. Matching – Ghép chữ Hán với nghĩa.
3. Pinyin Challenge – Ghép chữ với Pinyin.
4. Listening Quiz – Nghe và chọn.
5. Picture Quiz – Nhìn hình đoán từ.
6. Word Builder – Sắp xếp từ thành câu.
7. Speed Quiz – Trả lời nhanh.
8. Daily Challenge – Thử thách hàng ngày.

Yêu cầu:
- Có giao diện 2D sinh động.
- Có âm thanh phản hồi.
- Có hiệu ứng đúng/sai.
- Có điểm số.
- Có đồng hồ đếm giờ khi phù hợp.
- Có màn hình kết quả.
- Có nút chơi lại.
- Có lưu lịch sử.
- Có điều chỉnh độ khó.
- Không sử dụng dữ liệu câu hỏi giả cố định trong code sản phẩm.

## MODULE 08 – ÔN TẬP THÔNG MINH
- Tự động lưu từ đã học.
- Lưu từ trả lời sai.
- Tạo danh sách cần ôn.
- Nhắc ôn tập.
- Đánh giá mức độ ghi nhớ.
- Tự điều chỉnh lịch ôn dựa trên kết quả.
- Có chế độ ôn tập nhanh.

## MODULE 09 – ĐIỂM VÀ THÀNH TÍCH
- XP.
- Cấp độ.
- Huy hiệu.
- Chuỗi ngày học.
- Nhiệm vụ hàng ngày.
- Thành tích hoàn thành.
- Thống kê cá nhân.

Điểm phải được tính và xác thực ở phía máy chủ. Không cho phép học viên tự chỉnh sửa XP hoặc kết quả.

## MODULE 10 – PHỤ HUYNH
- Đăng nhập phụ huynh.
- Tạo và quản lý hồ sơ trẻ.
- Liên kết hồ sơ.
- Xem tiến độ.
- Xem thời gian học.
- Xem kết quả bài kiểm tra.
- Xem bài học hoàn thành.
- Xem từ vựng cần ôn.
- Thiết lập mục tiêu.
- Thiết lập nhắc học.

Phụ huynh chỉ được xem hồ sơ đã được liên kết và xác thực quyền.

## MODULE 11 – THỐNG KÊ
Dashboard hiển thị:
- Tổng số bài đã học.
- Tổng số từ vựng.
- Tổng thời gian học.
- Tỷ lệ hoàn thành.
- Điểm trung bình.
- Số ngày học liên tiếp.
- Tiến độ theo cấp độ.
- Biểu đồ theo ngày, tuần và tháng.

Dữ liệu dashboard phải lấy từ kết quả thật trong database.

## MODULE 12 – QUẢN TRỊ
Tạo trang quản trị riêng với các chức năng:

A. Quản lý tài khoản.

B. Quản lý học viên.

C. Quản lý phụ huynh.

D. Quản lý khóa học.

E. Quản lý cấp độ.

F. Quản lý chương.

G. Quản lý bài học.

H. Quản lý từ vựng.

I. Quản lý hình ảnh và âm thanh.

J. Quản lý câu hỏi và đáp án.

K. Quản lý trò chơi.

L. Quản lý thành tích.

M. Quản lý thông báo.

N. Báo cáo và thống kê.

O. Nhật ký hoạt động.

Mỗi chức năng quản trị phải có:
- Danh sách.
- Tìm kiếm.
- Lọc.
- Thêm mới.
- Chỉnh sửa.
- Xem chi tiết.
- Ẩn hoặc xuất bản.
- Xóa có xác nhận.
- Kiểm tra dữ liệu đầu vào.

## MODULE 13 – THÔNG BÁO VÀ HỖ TRỢ
- Thông báo trong ứng dụng.
- Nhắc học.
- Nhắc ôn tập.
- Hướng dẫn.
- FAQ.
- Gửi yêu cầu hỗ trợ.
- Quản lý phản hồi.

# V. THIẾT KẾ DATABASE

Hãy thiết kế PostgreSQL theo mô hình quan hệ, sử dụng UUID, khóa ngoại, index và RLS.

Các bảng tối thiểu:

1. profiles
2. user_roles
3. learner_profiles
4. parent_learner_links
5. parental_consents
6. user_settings
7. courses
8. levels
9. units
10. lessons
11. vocabulary
12. lesson_vocabulary
13. media_assets
14. example_sentences
15. quizzes
16. questions
17. question_options
18. enrollments
19. lesson_progress
20. learning_sessions
21. vocabulary_progress
22. review_schedules
23. game_sessions
24. game_answers
25. achievements
26. user_achievements
27. daily_goals
28. notifications
29. support_requests
30. audit_logs

Yêu cầu:
- Tạo migration SQL có thể chạy lại an toàn trong môi trường được chỉ định.
- Có khóa chính và khóa ngoại.
- Có ràng buộc dữ liệu.
- Có index.
- Có chính sách RLS.
- Có phân quyền theo vai trò.
- Có dữ liệu mẫu phục vụ kiểm thử.
- Không ghi đè database đang có.
- Không tự ý xóa dữ liệu.
- Không lưu mật khẩu trực tiếp.
- Không lưu secret trong frontend.

Trước khi tạo migration, phải xuất bản thiết kế ERD và giải thích quan hệ giữa các bảng.

# VI. MA TRẬN PHÂN QUYỀN

Các vai trò:

1. SUPER_ADMIN.
2. ADMIN.
3. CONTENT_EDITOR.
4. PARENT.
5. LEARNER.

Quy tắc:
- SUPER_ADMIN quản lý toàn bộ hệ thống.
- ADMIN quản lý người dùng, nội dung và báo cáo theo quyền được cấp.
- CONTENT_EDITOR quản lý nội dung học tập, không quản lý tài khoản hoặc dữ liệu nhạy cảm.
- PARENT quản lý và theo dõi hồ sơ trẻ được liên kết.
- LEARNER chỉ được truy cập hồ sơ, bài học và kết quả của chính mình.

Không được chỉ ẩn nút trên giao diện để tạo bảo mật. Phải kiểm tra quyền trên database và backend.

# VII. THIẾT KẾ GIAO DIỆN

Thiết kế theo phong cách 2D:

- Thân thiện.
- Hiện đại.
- Dễ sử dụng.
- Trẻ trung.
- Có minh họa hoạt hình.
- Tối ưu cho trẻ em nhưng không gây cảm giác quá trẻ con đối với người lớn.
- Responsive.

Màu sắc đề xuất:
- Đỏ Liên Hoa.
- Vàng.
- Trắng.
- Xanh dương.
- Xanh lá.

Tạo đầy đủ các màn hình:
1. Landing page.
2. Login.
3. Register.
4. Chọn hồ sơ.
5. Dashboard học viên.
6. Lộ trình.
7. Chi tiết bài học.
8. Flashcard.
9. Trò chơi.
10. Ôn tập.
11. Thành tích.
12. Thống kê.
13. Phụ huynh.
14. Quản trị.
15. Hồ sơ cá nhân.
16. Cài đặt.

Không tạo giao diện chỉ để trình diễn. Mọi nút phải thực hiện đúng hành động.

# VIII. YÊU CẦU KIẾN TRÚC CODE

- Phân chia module rõ ràng.
- Tách component.
- Tách service.
- Tách hooks.
- Tách types.
- Tách database queries.
- Tách business logic.
- Có xử lý loading.
- Có xử lý lỗi.
- Có trạng thái rỗng.
- Có thông báo thành công/thất bại.
- Có kiểm tra dữ liệu đầu vào.
- Không viết toàn bộ ứng dụng trong một file.
- Không lặp lại logic.
- Không dùng dữ liệu giả thay cho database thật.
- Không dùng localStorage làm nguồn dữ liệu nghiệp vụ chính.
- Có cơ chế quản lý biến môi trường.
- Có file README hướng dẫn chạy dự án.

# IX. BẢO MẬT VÀ DỮ LIỆU TRẺ EM

Đây là sản phẩm có đối tượng sử dụng là trẻ em, vì vậy phải ưu tiên bảo vệ dữ liệu cá nhân.

Bắt buộc:
- Xác thực người dùng.
- RLS.
- Kiểm tra quyền truy cập.
- Bảo vệ API.
- Không để lộ secret.
- Không công khai hồ sơ trẻ.
- Phụ huynh chỉ xem được hồ sơ đã liên kết.
- Có ghi nhận sự đồng ý cần thiết.
- Hạn chế thu thập dữ liệu cá nhân.
- Có quy trình yêu cầu xóa hoặc chỉnh sửa dữ liệu.
- Có audit log cho thao tác quản trị.
- Không triển khai quảng cáo hành vi hướng đến trẻ em.

Phải kiểm tra các yêu cầu pháp luật Việt Nam hiện hành về dữ liệu cá nhân và bảo vệ trẻ em trước khi phát hành chính thức.

# X. KIỂM THỬ

Phải thực hiện:

1. Unit test.
2. Integration test.
3. Authentication test.
4. Authorization test.
5. RLS test.
6. Database integrity test.
7. UI test.
8. Responsive test.
9. Game logic test.
10. Performance test.
11. Security test.

Các tình huống phải kiểm tra:
- Người A không xem được dữ liệu người B.
- Phụ huynh không xem được trẻ chưa liên kết.
- Học viên không truy cập trang quản trị.
- Editor không sửa được vai trò quản trị.
- Người dùng không tự tăng XP.
- Kết quả học không mất khi tải lại trang.
- Trò chơi lưu đúng kết quả.
- Dashboard khớp dữ liệu thực tế.
- Nội dung đã ẩn không xuất hiện trong lộ trình học.

Không được báo kiểm thử thành công nếu chưa thực sự chạy và ghi nhận kết quả.

# XI. KẾ HOẠCH THỰC HIỆN

Chia dự án thành 8 giai đoạn:

GIAI ĐOẠN 1: Phân tích và thiết kế.
GIAI ĐOẠN 2: Database và bảo mật.
GIAI ĐOẠN 3: Authentication và hồ sơ.
GIAI ĐOẠN 4: Hệ thống bài học.
GIAI ĐOẠN 5: Game và ôn tập.
GIAI ĐOẠN 6: Phụ huynh và quản trị.
GIAI ĐOẠN 7: Thống kê và thông báo.
GIAI ĐOẠN 8: Kiểm thử và phát hành.

Mỗi giai đoạn phải có:
- Mục tiêu.
- Danh sách công việc.
- File cần tạo hoặc sửa.
- Database cần thay đổi.
- Tiêu chí nghiệm thu.
- Kết quả kiểm thử.
- Những việc còn tồn tại.

# XII. NGÂN SÁCH

Tổng ngân sách không vượt quá 35 triệu VNĐ.

Nguyên tắc:
- Ưu tiên mã nguồn mở.
- Ưu tiên hạ tầng miễn phí hoặc chi phí thấp.
- Không tự ý mua dịch vụ.
- Không tự ý sử dụng API trả phí.
- Không phát sinh chi phí nếu chưa được phê duyệt.
- Báo cáo chi phí hạ tầng dự kiến theo tháng.
- Phân biệt chi phí phát triển và chi phí vận hành.

# XIII. NGUYÊN TẮC LÀM VIỆC VỚI SOURCE CODE

Nếu dự án đã có repository:

1. Kiểm tra repository trước.
2. Kiểm tra branch hiện tại.
3. Kiểm tra trạng thái Git.
4. Kiểm tra cấu trúc source code.
5. Kiểm tra package và dependencies.
6. Kiểm tra database hiện có.
7. Kiểm tra biến môi trường nhưng không in ra secret.
8. Kiểm tra chức năng đã tồn tại.
9. Lập báo cáo hiện trạng.
10. Lập kế hoạch thay đổi.

BẮT BUỘC:
- Tạo backup trước khi sửa.
- Không ghi đè source code đang hoạt động.
- Không xóa file nếu chưa có phê duyệt.
- Không xóa bảng hoặc dữ liệu database.
- Không tự ý đổi framework.
- Không tự ý đổi project Supabase.
- Không công khai repository riêng tư.
- Không commit secret.
- Không triển khai production khi chưa được phê duyệt.

Nếu chưa có repository, tạo cấu trúc dự án mới và hướng dẫn người quản lý phê duyệt nơi lưu source code.

# XIV. CƠ CHẾ KIỂM SOÁT TIẾN ĐỘ

Tạo file `PROJECT_STATUS.md` và cập nhật liên tục.

File phải có:
- Tiến độ tổng thể.
- Các module đã hoàn thành.
- Các module đang làm.
- Các module chưa làm.
- Lỗi đang tồn tại.
- Các quyết định kiến trúc.
- Các thay đổi database.
- Các bài kiểm thử đã chạy.
- Các rủi ro.
- Chi phí phát sinh.
- Công việc tiếp theo.

Tạo file `CHANGELOG.md` để lưu mọi thay đổi.

Tạo file `README.md` để hướng dẫn cài đặt và vận hành.

Không đánh dấu hoàn thành chỉ vì đã tạo file hoặc component. Chỉ đánh dấu hoàn thành khi chức năng chạy được và đã kiểm thử.

# XV. QUY TRÌNH THỰC HIỆN NGAY

Không được bắt đầu bằng cách viết code hàng loạt.

Hãy thực hiện theo thứ tự:

**BƯỚC 1:** Kiểm tra môi trường và repository.

**BƯỚC 2:** Báo cáo hiện trạng source code.

**BƯỚC 3:** Hoàn thiện BRD và SRS.

**BƯỚC 4:** Thiết kế kiến trúc tổng thể.

**BƯỚC 5:** Thiết kế ERD và database schema.

**BƯỚC 6:** Thiết kế ma trận phân quyền.

**BƯỚC 7:** Thiết kế wireframe và prototype.

**BƯỚC 8:** Lập kế hoạch triển khai theo module.

**BƯỚC 9:** Tạo backup và triển khai từng module.

**BƯỚC 10:** Kiểm thử và nghiệm thu từng module.

**BƯỚC 11:** Triển khai môi trường chạy thử.

**BƯỚC 12:** Bàn giao tài liệu và source code.

Ở mỗi bước phải có báo cáo kết quả trước khi chuyển sang bước tiếp theo.

# XVI. YÊU CẦU ĐẦU RA

Kết quả cuối cùng phải có:

1. Source code hoàn chỉnh.
2. Database schema.
3. Migration SQL.
4. RLS policies.
5. ERD.
6. BRD.
7. SRS.
8. Thiết kế UI/UX.
9. Ma trận phân quyền.
10. Bộ kiểm thử.
11. Báo cáo kết quả kiểm thử.
12. README.
13. CHANGELOG.
14. PROJECT_STATUS.
15. Hướng dẫn deploy.
16. Hướng dẫn quản trị.
17. Hướng dẫn sao lưu và phục hồi.
18. Danh sách các giới hạn còn tồn tại.

# XVII. LỆNH BẮT ĐẦU

BẮT ĐẦU TRIỂN KHAI DỰ ÁN LIÊN HOA KID NGAY.

Trước tiên, hãy thực hiện BƯỚC 1: kiểm tra repository, source code, môi trường, database và tình trạng hiện tại.

Chưa được sửa hoặc xóa bất kỳ dữ liệu nào ở bước đầu tiên.

Sau khi kiểm tra, hãy xuất báo cáo:

- Tổng quan hiện trạng.
- Công nghệ đang sử dụng.
- Những gì đã có.
- Những gì còn thiếu.
- Rủi ro kỹ thuật.
- Rủi ro bảo mật.
- Đề xuất cấu trúc hoàn thiện.
- Kế hoạch triển khai phù hợp ngân sách 35 triệu đồng.

Chờ xác nhận trước khi thực hiện những thay đổi có rủi ro hoặc ảnh hưởng đến dữ liệu.

**MỤC TIÊU CUỐI CÙNG: LIÊN HOA KID PHẢI LÀ MỘT SẢN PHẨM EDTECH CÓ THỂ SỬ DỤNG THỰC TẾ, KHÔNG PHẢI MỘT BẢN DEMO GIAO DIỆN.**