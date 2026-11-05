# Báo cáo kiểm thử OmniflowAI – HTML demo

## Đã thực hiện
- `node --check`: kiểm tra cú pháp JavaScript nhúng: đạt.
- Chạy Chromium headless bằng Playwright và `page.set_content` để nạp HTML.
- Khả năng hiển thị ở viewport 360, 390, 768, 1024, 1440, 1920 px: không có tràn chiều ngang **toàn trang** trên Dashboard.
- Kiểm tra 12 màn hình ở 390 và 1440 px = 24 tổ hợp: mỗi màn hình có nội dung, không có exception JS, không có tràn chiều ngang toàn trang.
- Menu mobile: mở sidebar và điều hướng đến Inbox thành công.
- Thao tác form: thêm sản phẩm, tạo đơn, soạn và gửi phản hồi nội bộ trong browser: đạt.
- Xuất ảnh chụp để kiểm tra trực quan Desktop Dashboard và Mobile Dashboard / Inbox.

## Kiểm tra còn cần thực hiện tại nơi triển khai
- Kiểm tra trực tiếp URL `file:///...` và URL GitHub Pages sau khi xuất bản: môi trường kiểm thử hiện tại chặn navigation tới file URL và máy chủ thử nghiệm, vì vậy không thể xác nhận bằng `page.goto` ở đây. Logic đã kiểm thử bằng cách nạp cùng HTML vào trình duyệt.
- Xác thực đa người dùng, database, đối soát đơn hàng, API Meta/Zalo/TikTok, chatbot AI thật: **chưa triển khai, không thể coi là đã test**.
- Kiểm tra Lighthouse/Core Web Vitals trên trang public: chưa thực hiện; không tuyên bố điểm số.

## Kết luận
Bản HTML là **frontend demo tương tác**, chưa phải SaaS production. Hai file HTML và ZIP được tạo từ cùng mã nguồn để đảm bảo đồng nhất giao diện tĩnh.
