# Privacy policies

Chính sách quyền riêng tư cho các ứng dụng Android (dùng làm "Privacy policy URL" trên Google Play).

| Ứng dụng | Trang |
|---|---|
| Máy Tính Việt / Tally Calculator (`com.moonchun.maytinh`) | `maytinh/` |

## Trước khi đẩy lên
Thay các chỗ giữ chỗ trong `index.html` và `maytinh/index.html`:
- `[TÊN NHÀ PHÁT TRIỂN]` / `[DEVELOPER NAME]`: tên hiển thị trên Google Play (tên tài khoản developer).
- `[EMAIL LIÊN HỆ]`: email liên hệ công khai (nên trùng email liên hệ khai trên Play Console).

## Đẩy lên GitHub và bật GitHub Pages
1. Tạo repo **public** tên `privacy` trên GitHub (không thêm README).
2. Trong thư mục này:
   ```bash
   git init
   git add .
   git commit -m "Privacy policies"
   git branch -M main
   git remote add origin https://github.com/<tài-khoản>/privacy.git
   git push -u origin main
   ```
3. Trên GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.
4. Sau 1–2 phút trang có ở: `https://<tài-khoản>.github.io/privacy/maytinh/`
   Mở thử bằng trình duyệt ẩn danh (không đăng nhập) để chắc trang công khai.
5. Dán link đó vào Play Console (App content → Privacy policy) và vào `AppConfig.privacyPolicyUrl` của app.

## Thêm app mới
Tạo thư mục `<tên-app>/index.html` theo mẫu `maytinh/`, sửa nội dung cho đúng dữ liệu app đó dùng, thêm một dòng vào `index.html`.

## Khi app thay đổi cách dùng dữ liệu
Ví dụ bật Firebase Crashlytics/Analytics: cập nhật trang của app (mục thu thập dữ liệu + ngày hiệu lực) **trước** khi phát hành bản đó, và cập nhật Data safety trên Play Console cho khớp.
