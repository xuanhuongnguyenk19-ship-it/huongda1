# Tín Đức ERP

Hệ thống quản trị doanh nghiệp cho Tín Đức, doanh nghiệp sản xuất LVL/Plywood. Hệ thống gồm các module: Sản xuất, Kho, Tài chính – Kế toán, Nhân sự, Dashboard Ban giám đốc và Quản trị hệ thống.

## Trạng thái

| Giai đoạn | Nội dung | Tình trạng |
|---|---|---|
| 1 | Phân tích nghiệp vụ | Đã có tài liệu, đang chờ xác nhận các câu hỏi |
| – | Bản thử giao diện (`ban-thu-web/`) | Đủ các module; đã làm chi tiết Công nợ và Kho (danh mục 3 cấp, 6 kho, xuất nhập kho); đã nạp sơ đồ tổ chức, chức danh, nhân viên và danh mục hàng hóa từ sheet “Thông tin hệ thống” |
| 2 | Thiết kế hệ thống: kiến trúc, CSDL, phân quyền | Chưa bắt đầu |
| 3–5 | Thiết kế giao diện, lập trình, hoàn thiện | Chưa bắt đầu |

## Cấu trúc thư mục

- `ban-thu-web/index.html`: bản thử chạy trong trình duyệt, dùng dữ liệu mẫu, lưu dữ liệu trong localStorage của từng máy.
- `ban-thu-web/HUONG-DAN.md`: hướng dẫn đưa bản thử lên web (Netlify, Vercel hoặc VPS).

## Lưu ý

Bản thử chỉ để xem giao diện và thử quy trình.

Bản thử có chứa dữ liệu thật lấy từ sheet “Thông tin hệ thống”: sơ đồ tổ chức, chức danh, danh mục hàng hóa và danh sách nhân viên. Với nhân viên, bản thử chỉ lấy mã, họ tên, phòng, nhóm, chức danh, trạng thái và ngày chính thức. Không lấy CCCD, số điện thoại, email, địa chỉ, ngày sinh, MST, mã BHXH hay tài khoản ngân hàng, và không nhập các thông tin này vào bản thử. Chỉ đưa bản thử lên đường link có mật khẩu.

Các số liệu khác trong bản thử (lương, đề xuất, công nợ, lệnh sản xuất, phiếu kho, giao việc) vẫn là dữ liệu mẫu.
