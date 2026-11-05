# OmniflowAI – kiến trúc triển khai production đề xuất

## 1. Lớp giao diện
- Tĩnh: GitHub Pages xuất bản `index.html` và tài nguyên công khai.
- SPA điều hướng bằng fragment (`#dashboard`, `#orders`, ...), thân thiện với đường dẫn con GitHub Pages.
- Tiếng Việt Unicode, semantic HTML, responsive, WCAG AA làm mục tiêu.

## 2. Lớp backend cần triển khai riêng
- Chọn dịch vụ: Cloudflare Workers + D1/R2/Queues, hoặc API Node.js/FastAPI tại dịch vụ riêng + PostgreSQL, tùy quy mô. Không coi chúng là đã cấu hình.
- Identity: xác thực, đổi mật khẩu, MFA, phiên đăng nhập, RBAC chủ shop/quản lý/nhân viên, multi-tenant.
- Dữ liệu: Shop, Channel, Conversation, Message, Customer, Product, InventoryMovement, Order, OrderItem, Campaign, AuditLog.
- Event flow: OAuth → webhook xác minh chữ ký → hàng đợi → idempotency → giao dịch DB → cập nhật realtime → API frontend.
- AI: thông tin được phép → kiểm soát dữ liệu cá nhân → retrieval trên FAQ/sản phẩm → model AI backend → kiểm tra output → nhân viên duyệt/gửi theo quyền.
- Bảo mật: mã hóa token tại server, phân quyền theo đối tượng, validate input, rate limiting, audit, backup, xóa dữ liệu theo yêu cầu.
- Analytics: số liệu tính từ bảng giao dịch, không hard-code lên dashboard.

## 3. API và các phụ thuộc bên thứ ba
Facebook/Instagram/Zalo/TikTok có chính sách, phạm vi quyền và thời hạn token riêng. Trước khi triển khai phải xác minh tài liệu nhà cung cấp, yêu cầu xét duyệt và loại tài khoản hợp lệ. Không hard-code secret trong JS tĩnh hoặc GitHub.

## 4. Giới hạn
GitHub Pages không chạy backend ứng dụng hoặc webhook. Việc triển khai `index.html` trên GitHub Pages bảo đảm cung cấp giao diện và logic demo, **không biến bản demo thành hệ thống bán hàng trực tuyến tự đồng bộ**.
