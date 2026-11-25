# Tiếp tục Bản Thảo bằng AI khác

Đọc file này trước, rồi AGENTS.md, docs/DEPLOYED_PAGES.md và docs/HANDOFF.md.

## Trạng thái hiện tại

**Web chính đã chạy độc lập trên Cloudflare Pages Free:** https://ban-thao-sonbi.pages.dev

- Pages project: `ban-thao-sonbi`; production branch: `main`.
- Web tĩnh, không R2, không Pages Functions, không hosting trả phí. Người dùng chỉ chấp nhận Free.
- `pages-free/assets/` là UI đang dùng; `pages-free/export.py` xuất dữ liệu từ app local.
- `desktop/` là collector/app Python 0.5.3. `web/` là source Sites cũ để tham khảo/quay lại, không phải UI của Pages hiện tại.
- Source gói này không chứa database, ảnh thật, phiên Telegram, cache phân loại hoặc token Cloudflare.

## Mẫu yêu cầu gửi AI

> Tiếp tục dự án Bản Thảo trong ZIP này. Giải nén, đọc START_HERE.md, AGENTS.md, docs/DEPLOYED_PAGES.md và docs/HANDOFF.md trước. Website chính là https://ban-thao-sonbi.pages.dev, project ban-thao-sonbi, chỉ dùng Cloudflare Pages Free, không R2/dịch vụ trả phí. Giữ dữ liệu gốc và phân loại đang có. Yêu cầu tiếp theo của tôi là: …

## Cách AI làm việc

1. Kiểm tra phiên bản và sửa đúng tầng. Đổi UI Pages thì sửa pages-free/assets, không chỉ sửa web/assets của Sites cũ.
2. Chạy test thích hợp. Bàn giao patch để người dùng chép vào tool trên Windows, bảo toàn data, .venv, pages-free/.local và phiên đăng nhập.
3. Người dùng mở app local rồi chạy CHAY_WEB_FREE.bat, chọn đúng project ban-thao-sonbi. Công cụ xuất toàn bộ thư viện và triển khai bản tĩnh mới.
4. Chỉ xác nhận deploy khi Wrangler báo thành công và link thực đã được kiểm tra. Đổi AI không tự cấp quyền quản trị Cloudflare; không yêu cầu gửi token/session/OTP vào chat.

Nếu AI chỉ có chat không có terminal, nó vẫn có thể đọc source và hướng dẫn/sửa file; không được khẳng định đã chạy test hoặc deploy thay người dùng.

## Git trong bản ZIP gọn

Bản dành cho Antigravity không kèm lịch sử Git để giảm dung lượng. Toàn bộ mã nguồn, skill và tài liệu vẫn đầy đủ. Giải nén rồi mở thư mục repo làm workspace. Có thể chạy git init, git add . và git commit để bắt đầu lịch sử mới; không cần repository.bundle.
