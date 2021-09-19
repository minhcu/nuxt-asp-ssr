# nuxt-asp-ssr

## asp

### 1. Khái niệm

- SPA (Single Page Application - Client Side Rendering) ứng dụng web chỉ hoạt động trên một trang (Không cần reload nguyên page)
- Thay vì gửi request đến server và reload trang thì SPA request server gửi về json để reload các component cần thiết.
- SPA sử dụng ajax để get dữ liệu cần thiết khi người dùng tương tác với website.

### 2. Quy trình

1. Khi truy cập website: Browser request Server sẽ trả về HTML-CSS
2. Xong HTML-CSS: Browser tiếp tục download JS
3. Xong JS: Browser executes JS(VUE)
4. JS executed: Web site đã có thể hiển thị và tương tác.

### 3. Ưu nhược điểm

#### a. Ưu điểm

- Nâng cao UX
- Server chỉ trả về JSON -> giảm tải tài nguyên trên Sever
- SPA hỗ trợ Progessive Web Apps, khi browser đã tải đủ các tài nguyên cần thiết, người dùng có thể sử dụng website mà không cần kết nối mạng.
- Dùng chung API: khi xây dựng API cho server, có thể sử dụng lại để build bản mobile.
- SPA vẫn yêu cầu front-end -> tạo công ăn việc làm

#### b. Nhược điểm

- Không thể sử dụng các kỹ thuật SEO advance
- SPA sử dụng rất nhiều JS -> Yêu cầu phải quản lý và code JS kỹ ->

## ssr

### 1. Khái niệm

- SSR (Server Side Rendering) là phương pháp hiển thị thông tin trên máy chủ. Browser request server, server sẽ thực hiện mọi thao tác logic và trả về thông tin để browser render.
- Khi tương tác với website, browser sẽ thực hiện gửi request để server xử lý.
- Khi truy cập 1 page bất kỳ, trình duyệt sẽ request server trả về nội dung page đó. Request phụ thuộc vào rất nhiều yếu tố khác nhau: tốc độ internet, vị trí máy chủ, lưu lượng truy cập hiện tại,...

### 2. Quy trình

1. Khi truy cập website: Trình duyệt gửi request lên server, trả về thông tin để Browser render.
2. Browser render HTML: Website đã được hiển thị, trong lúc này browser tiếp tục download JS.
3. JS downloaded: Browser executes JS.
4. JS executed: Website đã có thể tương tác được.

### 3. Ưu nhược điểm

#### a. Ưu điểm

- Dễ optimize vì toàn bộ dữ liệu đã được xử lý ở phía Server
- SEO tốt vì dữ liệu hiển thị dưới dạng HTML.
- Chạy tốt trên mọi trình duyệt.
- Phù hợp với static web.

#### b. Nhược điểm

- Thường xuyên request tới Server.
- Dễ gây bottleneck với web có quá nhiều hiệu ứng.
- Ít thân thiện với người dùng vì phải reload page.
- Khả năng tương tác không phong phú.

## Nuxt
