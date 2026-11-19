# Tín Đức ERP – bản thử: hướng dẫn đưa lên web

Thư mục này chỉ có **một file `index.html`**. Bản thử chạy hoàn toàn trên trình duyệt, không cần máy chủ hay cơ sở dữ liệu.

## Lưu ý quan trọng về dữ liệu

- Dữ liệu được lưu trong **bộ nhớ trình duyệt (localStorage) của từng máy**.
- Hai người mở cùng một đường link sẽ **không thấy dữ liệu của nhau**.
- Xóa lịch sử trình duyệt hoặc mở tab ẩn danh thì sẽ thấy lại dữ liệu mẫu ban đầu.
- Muốn quay về dữ liệu mẫu: đăng nhập thử bằng **Admin** → Quản trị → Quy trình duyệt & đơn giá → "Khôi phục dữ liệu mẫu ban đầu".
- Vì vậy bản này chỉ dùng để **xem giao diện và thử quy trình**, không dùng để nhập số liệu thật. Hệ thống thật (Giai đoạn 4) sẽ lưu dữ liệu tập trung trên VPS, có tài khoản đăng nhập và sao lưu.

## Cách 1 – Netlify Drop (nhanh nhất, không cần cài gì)

1. Mở https://app.netlify.com/drop
2. Đăng nhập hoặc tạo tài khoản Netlify (miễn phí).
3. Kéo cả thư mục `ban-thu-web` thả vào trang.
4. Netlify trả về một đường link dạng `https://ten-ngau-nhien.netlify.app`. Có thể đổi tên trong Site settings.

## Cách 2 – Vercel

1. Cài Node.js (đã có trên máy này), rồi mở PowerShell trong thư mục `ban-thu-web`.
2. Chạy `npx vercel` và đăng nhập khi được hỏi.
3. Trả lời các câu hỏi theo mặc định. Vercel sẽ trả về đường link.
4. Lần sau cập nhật thì chạy `npx vercel --prod`.

## Cách 3 – Đưa lên VPS đã thuê

Chép `index.html` vào thư mục web của máy chủ (ví dụ `/var/www/tinduc-thu/`), rồi cấu hình Nginx trỏ tên miền vào thư mục đó. Nên bật HTTPS (Let's Encrypt).

## Cần Internet để

- Tải font chữ *Be Vietnam Pro* (Google Fonts). Không có mạng thì trang dùng font hệ thống.
- Tải thư viện tạo mã QR (cdnjs). Không có mạng thì tem QR chỉ hiện chữ "QR".

## Bảo mật

- Trang không có mật khẩu: ai có đường link đều mở được.
- Chỉ dùng dữ liệu mẫu, không nhập thông tin thật của công ty, nhân viên hay khách hàng.
