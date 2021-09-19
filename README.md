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

#### 1. Ưu điểm

- Nâng cao UX
- Server chỉ trả về JSON -> giảm tải tài nguyên trên Sever
- SPA hỗ trợ Progessive Web Apps, khi browser đã tải đủ các tài nguyên cần thiết, người dùng có thể sử dụng website mà không cần kết nối mạng.
- Dùng chung API: khi xây dựng API cho server, có thể sử dụng lại để build bản mobile.
- SPA vẫn yêu cầu front-end -> tạo công ăn việc làm

#### 2. Nhược điểm

- Không thể sử dụng các kỹ thuật SEO advance
- SPA sử dụng rất nhiều JS -> Yêu cầu phải quản lý và code JS kỹ ->

## ssr

### 1. Khái niệm

