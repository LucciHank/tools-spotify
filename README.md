# TomOi Backup Spotify

Công cụ web giúp sao lưu và chuyển playlist Spotify giữa các tài khoản nhanh chóng và dễ dàng.

## Tính năng

- Xuất danh sách playlist và bài hát từ tài khoản Spotify
- Nhập danh sách vào tài khoản Spotify khác
- Giao diện đẹp, hiện đại và dễ sử dụng
- Hoàn toàn miễn phí và không lưu trữ dữ liệu người dùng

## Cách triển khai trên Vercel

1. Fork hoặc clone repository này về tài khoản GitHub của bạn
2. Đăng ký tài khoản Spotify Developer tại [https://developer.spotify.com/dashboard](https://developer.spotify.com/dashboard)
3. Tạo một ứng dụng mới trong Spotify Developer Dashboard
4. Cấu hình URL chuyển hướng (Redirect URI) trong ứng dụng Spotify là:
   - `https://tools.tomoi.vn/backup-spotify/login.html` (hoặc domain của bạn)
5. Cập nhật file `config.js` với thông tin ứng dụng Spotify của bạn:
   ```js
   config = {
       "uri":"https://tools.tomoi.vn/backup-spotify",
       "redirect_uri":"https://tools.tomoi.vn/backup-spotify/login.html",
       "client_id":"YOUR_CLIENT_ID",
       "client_secret":"YOUR_CLIENT_SECRET",
       "slowdown_import": 100,
       "slowdown_export": 100
   };
   ```
6. Tạo tài khoản trên [Vercel](https://vercel.com) và kết nối với GitHub
7. Tạo dự án mới trên Vercel và chọn repository GitHub chứa dự án này
8. Cấu hình build như sau:
   - Framework: Other
   - Build Command: Để trống
   - Output Directory: Để trống
9. Deploy và truy cập vào URL của dự án

## Kết quả triển khai

Sau khi triển khai thành công, ứng dụng sẽ có địa chỉ:
- https://tools.tomoi.vn/backup-spotify/ (nếu là subdirectory)
- https://backup-spotify.tools.tomoi.vn/ (nếu là subdomain)
- https://backup-spotify-username.vercel.app/ (nếu dùng domain mặc định của Vercel)

## Lưu ý quan trọng

- Đảm bảo đăng ký đúng URL chuyển hướng trong Spotify Developer Dashboard
- Thay đổi thông tin trong các file meta tags để tối ưu SEO cho website của bạn
- Cập nhật file `og-image.jpg` để hiển thị hình ảnh preview khi chia sẻ trên mạng xã hội

## Hỗ trợ

Nếu có bất kỳ vấn đề nào, vui lòng tạo issue trong repository này hoặc liên hệ thông qua website chính thức của [TomOi.vn](https://tomoi.vn).
