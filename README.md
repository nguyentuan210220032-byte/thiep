# Thiệp 20/10 — Mobile Motion 🌷

Thiệp chúc mừng ngày Phụ nữ Việt Nam, thiết kế **dọc cho điện thoại**, có phong bì mở 3D, cánh hoa rơi, chữ xuất hiện, thả tim và xem lại.

![Ảnh xem trước thiệp](./preview.png)

## Xem trên máy cá nhân

Mở `index.html` bằng trình duyệt. Nếu muốn kiểm tra với localhost trong VS Code, cài extension **Live Server**, chuột phải `index.html` → **Open with Live Server**.

> Không cần npm, Node.js, backend hay bước build. Chỉ dùng HTML, CSS và JavaScript thuần. Font Google yêu cầu kết nối internet; khi offline trình duyệt sẽ dùng font dự phòng.

## Đẩy lên GitHub

Tạo một repository trống trên GitHub, ví dụ `thiep-20-10` (không tick tạo README vì project đã có sẵn). Mở terminal **tại thư mục chứa `index.html`**:

```bash
git init
git add .
git commit -m "Create animated 20-10 greeting card"
git branch -M main
git remote add origin https://github.com/USERNAME/thiep-20-10.git
git push -u origin main
```

Thay `USERNAME` bằng tài khoản GitHub của bạn. Nếu repo đã khởi tạo và có `origin`, bỏ dòng `git init` / `git remote add origin` cho phù hợp.

## Xuất bản bằng GitHub Pages

1. Vào **GitHub repo → Settings → Pages**.
2. Tại **Build and deployment**, chọn **Deploy from a branch**.
3. Chọn branch `main` và folder `/ (root)`, nhấn **Save**.
4. Đợi GitHub triển khai xong. Đường dẫn thông thường:
   `https://USERNAME.github.io/thiep-20-10/`

Lưu ý: GitHub Pages cần repository và tài khoản hỗ trợ Pages theo chính sách GitHub. Khi sửa source, `git add . && git commit -m "Update card" && git push` để cập nhật trang.

## Chỉnh sửa nội dung và hiệu ứng

| Bạn muốn đổi | Mở file |
| --- | --- |
| Tiêu đề, lời chúc, câu ký tên | `index.html` |
| Màu hồng, font, bố cục responsive, animations | `assets/css/style.css` |
| Số cánh hoa rơi, lượng trái tim, hành vi các nút | `assets/js/main.js` |
| Biểu tượng trên tab trình duyệt | `assets/icons/favicon.svg` |

Để thay màu: sửa `--rose`, `--rose-dark`, `--gold`, `--bg` ở đầu file CSS.

## Cấu trúc source

```text
thiep-20-10/
├── index.html                   # Trang chủ GitHub Pages
├── assets/
│   ├── css/style.css            # Giao diện + animation
│   ├── js/main.js               # Tương tác
│   └── icons/favicon.svg        # Icon tab
├── preview.png                  # Ảnh minh hoạ README
├── .nojekyll                    # Cho phép GitHub Pages phục vụ file trực tiếp
├── .gitignore
└── README.md
```

Nếu muốn dùng domain riêng, thiết lập tại GitHub Pages và DNS; đừng tự thêm CNAME nếu chưa cấu hình domain.
