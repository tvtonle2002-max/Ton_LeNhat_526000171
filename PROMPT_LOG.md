# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

- **Họ và tên: Lê Nhất Tôn
- **MSSV: 526000171
- **Tên đề tài Website:** Website Trường học Ánh Dương
- **Công cụ AI đã sử dụng:** GitHub Copilot (Copilot SDK trong VS Code)

## 1. Yêu cầu ban đầu (System/Initial Prompt)

> Đóng vai một Frontend Developer chuyên nghiệp và tạo mã nguồn hoàn chỉnh cho website giới thiệu trường học bằng hai tệp `index.html` và `style.css`.
>
> Website cần sử dụng Semantic HTML5, bao gồm `header` với logo và điều hướng, `nav`, `main`, các `section` hoặc `article` để chia nội dung, và `footer` có thông tin liên hệ cùng bản quyền.
>
> Trong `style.css`, khai báo `:root` với các CSS Variables quản lý màu sắc, font chữ và spacing. Dùng Flexbox hoặc CSS Grid để tạo bố cục hiện đại, có responsive cơ bản trên thiết bị di động.
>
> Tích hợp Animate.css qua CDN trong phần `<head>` và áp dụng animation cho các nội dung chính. Tích hợp AOS qua CDN (CSS và JS), gắn `data-aos` cho các section. Tạo hiệu ứng `:hover` và `:focus` cho nút bấm, thẻ bài viết và khối thông tin. Xuất mã nguồn đầy đủ của hai tệp.

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Iterations)

### Lần 1: Dựng khung Semantic HTML & CSS Variable

- **Prompt đã dùng:** Yêu cầu tạo trang web giới thiệu trường học hoàn chỉnh, dùng HTML5 semantic, CSS Variables trong `:root`, bố cục Flexbox/Grid, responsive cơ bản và nội dung giới thiệu trường.
- **Kết quả AI tạo ra:** Tạo `index.html` và `style.css` với header, thanh điều hướng, hero, phần giới thiệu, sứ mạng/tầm nhìn, chương trình học, thành tựu và footer. CSS có biến màu sắc, font, spacing; các khối được bố trí bằng Grid/Flexbox và có breakpoint cho màn hình nhỏ.
- **Nhận xét & Tinh chỉnh của SV:** Cấu trúc nội dung dùng các thẻ semantic theo yêu cầu; bổ sung nội dung và hình ảnh minh họa để trang có đầy đủ các khu vực giới thiệu trường. Thông tin như tên trường, địa chỉ và số liệu trong bản mẫu cần được thay bằng dữ liệu thực tế trước khi sử dụng.

### Lần 2: Tích hợp thư viện Animate.css & AOS

- **Prompt đã dùng:** Yêu cầu tích hợp Animate.css và AOS từ CDN; thêm hiệu ứng cho tiêu đề, hero và nút bấm; gắn thuộc tính `data-aos` cho các section; bổ sung hiệu ứng hover/focus cho nút và card.
- **Kết quả AI tạo ra:** Thêm liên kết CDN Animate.css và AOS trong HTML, áp dụng lớp animation cho nội dung hero, khởi tạo AOS bằng JavaScript và gắn `data-aos` cho các phần nội dung. Bổ sung chuyển động hover, focus-visible, và hỗ trợ giảm chuyển động theo thiết lập của hệ điều hành.
- **Thách thức gặp phải:** AOS và Animate.css cần tải được các tệp từ CDN; nếu mất kết nối Internet hoặc CDN không truy cập được, các hiệu ứng tương ứng sẽ không hoạt động. Chưa phát hiện lỗi hiển thị trong quá trình kiểm tra cấu trúc tệp.
- **Cách sửa prompt (Debug prompt):** Yêu cầu nạp đủ CSS và JavaScript của AOS, gọi `AOS.init()` sau khi tải thư viện, đồng thời gắn `data-aos` trực tiếp lên các section cần hiệu ứng. Với Animate.css, thêm class hiệu ứng vào các phần tử cần hoạt ảnh và nạp stylesheet CDN trong `<head>`.

## 3. Đánh giá cá nhân về quá trình Vibe Coding

- **AI đã giúp bạn tiết kiệm thời gian ở phần nào nhất?** AI hỗ trợ dựng nhanh cấu trúc HTML, nội dung mẫu cho các khu vực của trang, hệ thống CSS Variables và các breakpoint responsive. Việc tích hợp thư viện animation cũng được thực hiện đồng bộ trong cùng bộ mã nguồn.
- **Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web?** Nên nêu rõ cấu trúc semantic, tên tệp, thư viện cần tích hợp, hành vi mong muốn, yêu cầu responsive và trạng thái tương tác. Khi tinh chỉnh, mô tả cụ thể vị trí cần hiệu ứng và cách khởi tạo thư viện sẽ giúp kết quả dễ kiểm tra hơn. Cần rà soát lại nội dung mẫu, dữ liệu liên hệ và hình ảnh trước khi đưa website vào sử dụng thực tế.