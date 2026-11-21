# Chạy local bằng Supabase + Docker

Chưa có project Supabase trên cloud. Giai đoạn phát triển dùng Supabase local (Docker). Khi ra mắt thật, tạo project cloud rồi đẩy migration lên.

## Yêu cầu
- Docker đang chạy trên máy của bạn.
- Node 20+ và npm.
- Supabase CLI (cài qua npm: `npm i -D supabase`, hoặc theo hướng dẫn chính thức).

## Lệnh cơ bản (sau khi có `supabase/config.toml`)
```bash
npx supabase start        # khởi động Postgres, Auth, Storage, Studio bằng Docker
npx supabase db reset     # chạy lại toàn bộ migration + seed (chỉ dùng cho local)
npx supabase status       # xem URL và key local
npx supabase stop
```
Điền URL và anon key local vào `.env.local` (copy từ `.env.example`). **Không commit `.env.local`.**

## Khi lên cloud
1. Tạo project Supabase mới (bạn tạo, mình không tự ý tạo hay mua dịch vụ).
2. `npx supabase link --project-ref <ref>` rồi `npx supabase db push`.
3. Đặt biến môi trường production trên hosting; không đưa `service_role` vào frontend.

## Ghi chú
- Mọi thay đổi database đi qua file trong `supabase/migrations/`, không sửa tay trên production.
- `db reset` xóa dữ liệu local, tuyệt đối không chạy trên môi trường thật.
