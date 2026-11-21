# PROJECT STATUS – LIÊN HOA KID (LHK-2026-001)

Cập nhật: 2026-11-21

## Tiến độ tổng thể
Giai đoạn 1 (Phân tích và thiết kế): đang làm. Chưa có code sản phẩm.

## Module
| Nhóm | Trạng thái |
|---|---|
| Hoàn thành | Không có |
| Đang làm | Khởi tạo repo, ERD, ma trận phân quyền |
| Chưa làm | Toàn bộ 13 module (xem Master Prompt mục IV) |

## Lỗi đang tồn tại
Không có (chưa có code).

## Quyết định kiến trúc
- D-01: Repo Git cục bộ tại `lien-hoa-kid/`, người quản lý tự đẩy lên remote sau.
- D-02: Stack theo Master Prompt: React + TypeScript + Vite, Supabase (Auth, PostgreSQL, Storage), PWA.
- D-03 (chốt 2026-11-21): Học sinh tự đăng ký tài khoản riêng. Dưới ngưỡng tuổi cần phụ huynh xác nhận (ngưỡng tạm 16, chờ đối chiếu pháp luật VN). Phụ huynh vẫn có thể tạo hồ sơ cho trẻ nhỏ.
- D-04: XP/điểm ghi qua hàm RPC phía máy chủ, khóa ghi trực tiếp từ client.
- D-05 (chốt 2026-11-21): Chưa có project Supabase cloud; phát triển bằng Supabase local qua Docker (xem `docs/SETUP_LOCAL.md`).
- D-06 (chốt 2026-11-21): Giữ nguyên cấu trúc 30 bảng và cây thư mục; tài liệu do AI viết.
- D-07: Giữ phạm vi full, gắn mức P1/P2 trong `docs/SRS.md` để ưu tiên theo tiến độ.

## Thay đổi database
Chưa có migration nào. ERD: `docs/ERD.md` (chờ duyệt trước khi viết migration).

## Kiểm thử đã chạy
Chưa có.

## Rủi ro
1. Phạm vi full 13 module so với 8 tuần và 35 triệu: nguy cơ cao.
2. Hồ sơ v1.0 và Master Prompt lệch phạm vi (11 so với 16 màn hình; 5 so với 15 nhóm quản trị).
3. Học liệu HSK 1–6 và âm thanh chưa có nguồn, bản quyền cần xác minh.
4. Dữ liệu trẻ em: cần rà soát pháp luật Việt Nam trước phát hành.

## Chi phí phát sinh
0 đ. Hạ tầng dự kiến: Supabase Free khi phát triển; gói trả phí khi chạy thật (cần xác nhận giá hiện hành).

## Tài liệu đã viết
`docs/BRD.md`, `docs/SRS.md`, `docs/ERD.md`, `docs/PERMISSIONS.md`, `docs/SETUP_LOCAL.md`.

## Chờ xác nhận
- Ngưỡng tuổi cần phụ huynh xác nhận (tạm 16) và thời hạn lưu hồ sơ chưa xác nhận.
- Học liệu: đã có hay soạn bộ mẫu? Nguồn âm thanh phát âm.
- Duyệt ERD (bản cập nhật) và ma trận phân quyền.

## Công việc tiếp theo
Sau khi duyệt: Giai đoạn 2, viết migration SQL, RLS, RPC; kiểm thử trên Postgres 16 và qua `supabase db reset` trên máy có Docker.
