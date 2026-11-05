# OMNIFLOW AI — HUONG DAN SU DUNG VA TRIỂN KHAI

## 1. Mở ngay trên máy tính
Mở file `OmniflowAI_Preview.html` hoặc `index.html` bằng trình duyệt.
Hai file này có cùng nội dung chính xác 100%, bao gồm cấu trúc HTML, CSS, JavaScript, các biểu tượng đồ họa, màu sắc và dữ liệu mẫu.
Không cần cài thư viện hay tải thêm hình ảnh cho giao diện hiện tại.

## 2. Triển khai GitHub Pages
1. Mở repository https://github.com/iennhi141105-star/OmniflowAI
2. Upload **nội dung bên trong ZIP**, không upload nguyên ZIP; bảo đảm `index.html` nằm ngay thư mục gốc của nhánh `main`.
3. Vào Settings > Pages > Build and deployment > Deploy from a branch; chọn `main` và `/(root)`; Save.
4. Đường dẫn dự kiến (sau khi chủ kho thực sự bật Pages): https://iennhi141105-star.github.io/OmniflowAI/

## 3. Bảo đảm giao diện
`index.html` và `OmniflowAI_Preview.html` có cùng SHA-256 in trong `CHECKSUMS.sha256`.
Cả hai tự chứa CSS, JS và biểu tượng. Các ảnh trong `anh-giao-dien/` là ảnh chụp tham khảo, không cần thiết để chạy trang.
Font hiện tại dựa trên chuỗi `Segoe UI`, `Arial`, `system-ui`, `sans-serif`: nếu chạy trên hai hệ điều hành khác nhau, browser có thể chọn font fallback khác, khiến chữ hiển thị khác nhẹ. Hai file không có khác biệt CSS/font.
Dữ liệu thao tác được lưu theo trình duyệt và origin (`localStorage`); trạng thái sau sử dụng có thể khác nhau giữa file local và URL GitHub dù mã nguồn giống hệt.

## 4. Giới hạn
Đây là demo frontend tương tác dùng dữ liệu cục bộ. Facebook, Instagram, Zalo, livestream, API AI, backend và đồng bộ thực chưa được kết nối. GitHub Pages không tự chạy backend.
Không đưa khóa API/mật khẩu lên GitHub.
