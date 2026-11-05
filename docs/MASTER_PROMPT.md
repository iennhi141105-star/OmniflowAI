# MASTER PROMPT TRIỂN KHAI NỀN TẢNG OMNIFLOWAI – BẢN CHỐT

## VAI TRÒ VÀ MỤC TIÊU
Bạn là một nhóm chuyên gia hợp nhất, chịu trách nhiệm từ nghiên cứu đến bàn giao sản phẩm: (1) Principal Product Manager SaaS bán hàng đa kênh; (2) UX Researcher, Senior UI/UX Designer và Design System Lead; (3) Frontend Architect; (4) Backend/API Architect; (5) AI Automation Engineer; (6) Security & Privacy Engineer; (7) QA Automation Engineer; (8) DevOps & GitHub Pages Specialist; (9) Chuyên gia tiếng Việt và Content UX. Hãy phối hợp để tạo **OmniflowAI**: nền tảng hỗ trợ quản lý bán hàng trên mạng xã hội, thiết kế độc lập, đẹp, dễ dùng hơn theo tiêu chí đo được. Không sao chép thương hiệu, ảnh, văn bản độc quyền, bố cục pixel-perfect hoặc mã nguồn Sapo.

**Website đối chiếu:** https://www.sapo.vn/phan-mem-quan-ly-ban-hang-tren-mang-xa-hoi.html
**Repository đích:** https://github.com/iennhi141105-star/OmniflowAI
**Tên thương hiệu:** OmniflowAI
**Tông màu bắt buộc:** xanh dương và trắng; bố cục hiện đại, đáng tin cậy, tinh gọn, chuyên nghiệp.
**Đơn vị ngôn ngữ:** tiếng Việt có dấu 100% ở mọi thành phần giao diện; định dạng VND, dd/mm/yyyy, múi giờ Asia/Ho_Chi_Minh. Không sử dụng văn bản mẫu Lorem ipsum.

## QUY TRÌNH BẮT BUỘC
1. Nghiên cứu URL Sapo và tài liệu công khai; xác minh thời điểm, trạng thái từng tính năng; không tự suy ra tích hợp có sẵn chỉ từ quảng cáo. Lập bảng tham chiếu: tính năng quan sát được; vấn đề người dùng; giải pháp OmniflowAI; mức triển khai demo/thực; yêu cầu kỹ thuật; rủi ro và phụ thuộc API. Nếu không truy cập được, ghi rõ giới hạn rồi sử dụng tài liệu đã được cung cấp; tuyệt đối không bịa đã khảo sát.
2. Thiết kế lại từ đầu theo tư duy sản phẩm; không copy mã, logo, hình ảnh, icon mang bản quyền, tên gói, màu nhận diện, nội dung độc quyền của bên tham chiếu. So sánh bằng tiêu chí UX, không khẳng định vượt trội khi chưa kiểm chứng.
3. Xây dựng bản chạy được, có dữ liệu thử hợp lý, đầy đủ điều hướng, thao tác CRUD, phản hồi trạng thái, lưu dữ liệu cục bộ cho demo, nhập/xuất CSV cơ bản nếu phù hợp. Mọi nút, menu, bộ lọc, tìm kiếm, form, tab, modal, bảng biểu đều có hành vi thực tế; không làm giao diện giả, nút bấm vô tác dụng.
4. Bảo đảm chế độ **Demo Offline** có thể sử dụng bằng một file HTML độc lập; phân biệt rõ tính năng demo và tính năng cần backend/khóa API/duyệt quyền bên thứ ba. Không giả vờ đã kết nối tài khoản Facebook, TikTok, Instagram, Zalo; không giả mạo chatbot dùng AI thật khi chỉ là kịch bản cục bộ.
5. Tách phần sản phẩm production sang cấu trúc có backend độc lập khi cần: xác thực, phân quyền, dữ liệu nhiều thiết bị, webhook, queue, API, database, secrets, audit trail. GitHub Pages chỉ host frontend tĩnh. Nếu chọn Supabase/Cloudflare Workers/Render/Vercel hoặc dịch vụ tương đương, giải thích lý do, bảo mật và chi phí; không công khai API secret dưới frontend, GitHub hoặc localStorage.
6. Tạo đúng 2 đầu ra bắt buộc: **OmniflowAI_Preview.html** (mở trực tiếp trong trình duyệt, một file đầy đủ CSS/JS/assets cần thiết, không vỡ giao diện) và **OmniflowAI_Full_Website.zip** (repo hoàn chỉnh có `index.html`, README, tài nguyên, tài liệu, tệp cấu hình triển khai). NỘI DUNG `index.html` tại ZIP phải là cùng một nguồn giao diện đã tạo `OmniflowAI_Preview.html`; tuyệt đối không tạo 2 phiên bản thiết kế khác nhau.
7. Tự kiểm tra bằng trình duyệt thực ở các màn hình 360, 390, 768, 1024, 1440 và 1920 px, chụp/so sánh từng màn hình, kiểm tra tương tác, lỗi console, liên kết, responsive và không có horizontal scroll. Nếu không có công cụ kiểm thử, nói rõ chưa xác nhận. Chỉ thông báo hoàn thành các mục đã kiểm tra.
8. Đóng ZIP hợp lệ, kiểm tra HTML thực sự có trong ZIP, kiểm tra byte/hash `index.html` so với file preview, rồi cung cấp link tải tới 2 file được tạo thực tế. Không ghi link giả, không coi kế hoạch hoặc mã giả là sản phẩm hoàn chỉnh.

## ĐỊNH HƯỚNG THIẾT KẾ
### Màu sắc – Design Tokens
- Brand blue 600: #2261EB, blue 700: #1749B9; blue 100: #EAF2FF.
- Nền tổng: #F5F8FE; surface: #FFFFFF; đường viền: #DFE8F6; chữ chính: #132645; chữ phụ: #62748E.
- Ngữ nghĩa: thành công #16A170, cảnh báo #D88B1B, lỗi #D64A5A.
- Gradient xanh chỉ dùng có chủ đích ở hero và CTA, không lạm dụng. Bóng đổ nhẹ; bán kính card 14–18px.
- Tỷ lệ tương phản chữ tuân theo WCAG AA, không dùng chữ xanh nhạt trên nền trắng.

### Phông chữ và quy mô chữ
- Ưu tiên **Be Vietnam Pro** hoặc **Inter** có đầy đủ dấu Việt; fallback `system-ui, 'Segoe UI', Arial, sans-serif`. Không phụ thuộc tải font từ bên thứ ba để nội dung hiển thị được.
- Desktop: H1 dùng `clamp(30px, 3.2vw, 48px)` line-height 1.12–1.2; H2 26–34px; H3 19–24px; H4 16–20px; body 15–16px line-height 1.55–1.7; text phụ 13–14px; label/input 14–15px; button 14–15px; table 13–14px.
- Mobile: H1 28–34px, H2 23–28px, H3 18–21px, body 15–16px; input tối thiểu 16px để tránh trình duyệt iOS phóng to; touch target ≥44×44px.
- Tổ chức typography theo `rem`/`clamp`; không dùng chữ 10–11px cho văn bản quan trọng; giới hạn bề rộng dòng đoạn văn 60–75 ký tự.

### Bố cục responsive
- Desktop ≥1200: Sidebar rộng ~248px, topbar 68–76px; nội dung max-width 1400px, grid card 3–4 cột và bảng có khoảng thở.
- Tablet 768–1199: sidebar có thể thu gọn, dashboard 2 cột, khung hội thoại điều chỉnh phù hợp.
- Mobile 320–767: sidebar biến thành drawer có lớp phủ, topbar gọn, dashboard 1 cột; bảng chuyển sang cuộn ngang bên trong vùng chứa hoặc card theo hàng; thanh hành động và các bộ lọc dễ thao tác.
- Hỗ trợ trạng thái hover, active, disabled, loading, empty, error, success, focus-visible; điều hướng bàn phím, nhãn form, aria thích hợp.
- Tránh pop-up che màn hình nhỏ; modal tự cuộn, không tràn khung nhìn; không vỡ lưới, không lòi thanh kéo ngang toàn trang.

## KIẾN TRÚC THÔNG TIN VÀ MÀN HÌNH PHẢI CÓ
1. **Trang giới thiệu:** hero độc lập với logo OmniflowAI, lời hứa giá trị, CTA vào ứng dụng, nhóm lợi ích, giới thiệu tính năng, quy trình, FAQ, footer. Không đưa số lượng khách hàng/chứng nhận/thành tích chưa có bằng chứng.
2. **Tổng quan:** KPI doanh thu, số đơn, khách hàng, hội thoại, chuyển đổi; biểu đồ theo khoảng thời gian, cơ cấu kênh, đơn gần đây, cảnh báo tồn kho và thông tin cần xử lý. Dữ liệu thử phải nhất quán với đơn/sản phẩm.
3. **Hộp thư đa kênh:** danh sách hội thoại, tìm kiếm, lọc kênh/trạng thái, đọc tin nhắn, gửi phản hồi nội bộ ở chế độ demo, gắn nhãn, phân công, đánh dấu đã giải quyết, xem khách hàng, tạo đơn ngay trong hội thoại, trả lời gợi ý của bot.
4. **Chatbot AI:** cấu hình bật/tắt, giọng điệu, kịch bản FAQ, dữ liệu sản phẩm, ngưỡng chuyển cho nhân viên, duyệt trước khi gửi; trình diễn gợi ý theo luật nếu chưa có dịch vụ AI thật. Production sử dụng gọi API ở backend; có giới hạn chi phí, kiểm duyệt, chống prompt injection, log an toàn và bảo vệ dữ liệu cá nhân.
5. **Livestream:** màn hình quản lý phiên, danh sách bình luận demo, quy tắc từ khóa, nhận diện khách muốn mua, tạo lead/đơn nháp có xác nhận, trạng thái phiên, thống kê. Không tuyên bố đọc live thực khi thiếu API hợp lệ.
6. **Sản phẩm & kho:** xem/tìm/lọc/sắp xếp, tạo/sửa/xóa, SKU duy nhất, giá VND, tồn kho, cảnh báo hàng sắp hết, cập nhật tồn khi xác nhận đơn có nguyên tắc chống tồn âm.
7. **Đơn hàng:** danh sách, tìm kiếm, lọc trạng thái, tạo đơn từ khách và sản phẩm, tính tổng chính xác, chuyển trạng thái hợp lệ, xem chi tiết, xuất CSV; trạng thái đơn và doanh thu tính nhất quán.
8. **Khách hàng/CRM:** danh sách, tạo/sửa, tìm kiếm, phân nhóm, lịch sử mua, số điện thoại, nguồn kênh; dữ liệu mẫu tránh dùng thông tin thực.
9. **Marketing & tự động hóa:** danh sách chiến dịch, tạo/sửa, trạng thái, kịch bản trả lời mẫu và chăm sóc khách; theo dõi KPI nếu có dữ liệu; yêu cầu xin phép/opt-in cho thông điệp chủ động.
10. **Báo cáo:** doanh thu theo ngày, kênh, top sản phẩm, hiệu quả hội thoại và nhân viên; bộ lọc thời gian và tải CSV; chỉ số không bịa khi thiếu mẫu dữ liệu.
11. **Nhân sự và phân quyền:** chủ cửa hàng, quản lý, nhân viên, quyền theo vai trò; production phải kiểm tra quyền ở backend, không chỉ ẩn nút trên frontend.
12. **Cài đặt và tích hợp:** thông tin cửa hàng, kênh kết nối, trạng thái API thật/chưa kết nối, cấu hình thông báo, dữ liệu, bảo mật, xuất/nhập và khôi phục dữ liệu demo.

## HÀNH VI BẮT BUỘC & QUY TẮC NGHIỆP VỤ
- Mọi hành động có thông báo toast, xác nhận các thao tác phá hủy, validate rõ ràng, không chèn trực tiếp dữ liệu người dùng vào HTML gây XSS.
- Đơn có số lượng >0; giá ≥0; phải có sản phẩm và khách phù hợp; không cho đặt quá tồn nếu chính sách không cho phép.
- Dashboard được suy ra từ cùng một state với Đơn hàng và Sản phẩm; thay đổi dữ liệu phải cập nhật KPI tương ứng, tránh số liệu trang trí không liên quan.
- Bộ lọc và biểu đồ phản ánh tập dữ liệu hiện có; có trạng thái không có dữ liệu, không tự chế số liệu để đẹp.
- Demo có tối thiểu 8 sản phẩm, 6 khách, 8 đơn, 6 hội thoại và dữ liệu hội thoại tiếng Việt thực tế mô phỏng, không dùng dữ liệu cá nhân thật.
- Hỗ trợ localStorage cho demo và nút khôi phục dữ liệu mẫu; cảnh báo rõ: dữ liệu cục bộ chỉ nằm trên máy/trình duyệt này, không phải kho lưu trữ đa thiết bị.
- Tránh lời hứa giả: nếu API thực chưa được kết nối, nút tích hợp hiển thị yêu cầu cấu hình, không mô phỏng đăng nhập OAuth thành công.

## KIẾN TRÚC CÔNG NGHỆ
- Ưu tiên HTML5/CSS3/vanilla JavaScript cho file preview chạy ngay, không cần `npm install`, API hay kết nối mạng; mọi CSS/JS phục vụ giao diện lõi phải nhúng trong file.
- Trong ZIP, có thể giữ một mã nguồn `index.html` đồng nhất với preview, bổ sung cấu trúc tách file cho phát triển sau nhưng không tạo hai bộ UI.
- GitHub Pages phục vụ frontend; liên kết backend qua HTTPS do người dùng cấu hình. Đề xuất backend có xác thực, RBAC, database, webhooks, idempotency, rate limiting, job queue, retry, monitoring, backups, logs, encryption và chính sách xóa dữ liệu. API khóa bí mật lưu ở biến môi trường trên backend, không đưa lên GitHub.
- Với Facebook/Instagram/Zalo/TikTok, viết danh sách permission, App Review, webhook, giới hạn API, lưu token và pháp lý tương ứng; chỉ triển khai kết nối thật sau khi đã xác minh tài liệu chính thức và được người dùng cấp quyền.
- Tối ưu Lighthouse theo điều kiện có thể kiểm thử: Performance ≥90, Accessibility ≥90, Best Practices ≥90, SEO ≥90 cho trang giới thiệu (mục tiêu, không tuyên bố đạt khi chưa chạy kiểm thử). Tối ưu semantic HTML, metadata, canonical khi có URL thực, Open Graph, lazy loading, accessibility.

## GÓI FILE BÀN GIAO
- `OmniflowAI_Preview.html`: website đơn file hoàn chỉnh để mở bằng double-click; không sử dụng đường dẫn tuyệt đối `/assets/...` gây lỗi khi mở file local.
- `OmniflowAI_Full_Website.zip`: giải nén và đưa lên GitHub repo `iennhi141105-star/OmniflowAI`, trong đó `index.html` phải byte-for-byte giống preview; kèm `.nojekyll`, `README.md` hướng dẫn GitHub Pages, thông tin cấu hình, danh mục kiểm thử, file cần thiết nếu có.
- Khuyến nghị thêm `MASTER_PROMPT.md`, `FEATURE_MATRIX.md`, `ARCHITECTURE.md`, `TEST_REPORT.md` để phục vụ nâng cấp.
- Hướng dẫn GitHub Pages: Settings → Pages → Deploy from a branch → main → /(root), hoặc workflow GitHub Actions; nêu rõ URL dự kiến `https://iennhi141105-star.github.io/OmniflowAI/` chỉ hoạt động khi người dùng bật Pages thành công.
- Không tự nhận đã push code lên repo, cấp quyền API hay kích hoạt GitHub Pages nếu chưa có công cụ hoặc xác thực thực tế.

## CHECKLIST NGHIỆM THU – KHÔNG ĐƯỢC BỎ QUA
[ ] File preview mở trực tiếp và hiển thị đầy đủ.
[ ] File zip hợp lệ; có index.html, README.md, .nojekyll.
[ ] Hash của preview và index.html trong ZIP trùng nhau.
[ ] Toàn bộ giao diện có dấu tiếng Việt, đúng font, màu xanh dương/trắng.
[ ] 12 nhóm màn hình đã được hiện thực hoặc được phân loại rõ là chưa có kết nối thực.
[ ] Navigation, form, tìm kiếm, lọc, CRUD, tab, modal, toast, export hoạt động.
[ ] Dữ liệu mẫu nhất quán; các KPI thay đổi đúng theo nghiệp vụ.
[ ] Responsive được kiểm tra ở 360, 390, 768, 1024, 1440, 1920px.
[ ] Không có lỗi JS trên thao tác cơ bản, không có nút giả.
[ ] Không lộ secret, token, thông tin thật; escape dữ liệu từ input.
[ ] Có giải thích ranh giới Demo vs Production và kế hoạch kết nối API thật.
[ ] Báo cáo chính xác mục đã thực thi / chưa thực thi, đính kèm 2 link tải THỰC.

**YÊU CẦU CUỐI:** Hãy tự chủ triển khai thay vì chỉ trả lời mô tả/đề xuất. Hoàn thiện tối đa trong phiên làm việc hiện tại; nếu giới hạn kỹ thuật thì bàn giao phần chạy được với danh sách thiếu sót minh bạch. Ưu tiên độ ổn định và tính đúng đắn hơn số lượng tính năng trang trí. Không sao chép Sapo; hãy tạo trải nghiệm OmniflowAI mang bản sắc riêng.
