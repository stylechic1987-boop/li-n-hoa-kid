# LIÊN HOA KID

Nền tảng học tiếng Trung độc lập (web + PWA, giao diện 2D) của Liên Hoa Global Education. Mã dự án LHK-2026-001.

## Trạng thái
Đang ở giai đoạn thiết kế. Chưa có code chạy được. Xem `PROJECT_STATUS.md`.

## Cấu trúc
```
docs/            Tài liệu: ERD, phân quyền, nguồn gốc
docs/source/     Hồ sơ thiết kế v1.0 và Master Prompt (bản gốc)
supabase/        migrations, seed, tests
src/             Frontend React + TypeScript (sẽ khởi tạo)
e2e/             Kiểm thử Playwright
```

## Công nghệ
React, TypeScript, Vite, Tailwind CSS, Supabase (Auth, PostgreSQL, Storage), PWA, Vitest, Playwright.

## Chạy dự án
Chưa khả dụng. Hướng dẫn cài đặt sẽ được bổ sung khi khởi tạo frontend (Giai đoạn 2).

## Bảo mật
- Không commit file `.env`. Dùng `.env.example` làm mẫu.
- Không đưa `service_role` key vào frontend.

## Đẩy lên remote
Repo mới chỉ có Git cục bộ (nhánh `main`). Khi sẵn sàng: `git remote add origin <url>` rồi `git push -u origin main`.
