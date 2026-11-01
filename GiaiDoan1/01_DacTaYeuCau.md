# Giai đoạn 1 - Đặc tả yêu cầu

## 1. Mục tiêu hệ thống
Hệ thống quản lý đặt lịch và dịch vụ trực tuyến hỗ trợ khách hàng đặt lịch, thanh toán, theo dõi tiến độ và nhận thông báo. Hệ thống cũng hỗ trợ nhân viên xử lý đơn và quản trị viên quản lý dịch vụ, người dùng và báo cáo.

## 2. Đặc tả yêu cầu chức năng

### 2.1 Quản lý người dùng
- Khách hàng có thể đăng ký, đăng nhập, cập nhật hồ sơ và đổi mật khẩu.
- Hệ thống phân quyền theo 3 vai trò: Khách hàng, Nhân viên, Quản trị viên.
- Quản trị viên có thể quản lý tài khoản, khóa/mở khóa tài khoản và phân quyền.

### 2.2 Quản lý dịch vụ
- Khách hàng xem danh sách dịch vụ, thông tin chi tiết và giá cả.
- Nhân viên và quản trị viên có thể thêm, sửa, xóa hoặc tạm dừng dịch vụ.
- Mỗi dịch vụ có mã, tên, mô tả, giá, thời lượng và trạng thái.

### 2.3 Quản lý đặt lịch
- Khách hàng chọn dịch vụ, ngày và khung giờ phù hợp.
- Hệ thống kiểm tra lịch trống và lưu thông tin đặt lịch.
- Khách hàng có thể xem lịch sử đơn, hủy hoặc đổi lịch theo quy định.

### 2.4 Thanh toán
- Khách hàng thanh toán trước hoặc thanh toán tại chỗ.
- Hệ thống lưu mã giao dịch, trạng thái thanh toán và thời gian thực hiện.
- Nhân viên và quản trị viên có thể xem thông tin thanh toán liên quan.

### 2.5 Quản lý xử lý đơn
- Nhân viên xem danh sách lịch hẹn được giao.
- Nhân viên cập nhật trạng thái: chờ xác nhận, đã xác nhận, đang thực hiện, hoàn thành, hủy.
- Nhân viên ghi nhận kết quả và cập nhật tiến độ thực hiện.

### 2.6 Thông báo
- Hệ thống gửi nhắc lịch trước giờ hẹn.
- Gửi thông báo xác nhận, hoàn thành hoặc hủy lịch.
- Khách hàng nhận thông báo qua email, SMS hoặc ứng dụng.

### 2.7 Báo cáo và thống kê
- Quản trị viên xem báo cáo doanh thu theo ngày/tháng.
- Hệ thống thống kê số đơn, tỷ lệ hoàn thành, số lượng hủy lịch.
- Có thể xuất báo cáo PDF/Excel.

## 3. Đặc tả yêu cầu phi chức năng

### 3.1 Hiệu năng
- Thời gian phản hồi màn hình dưới 3 giây ở mức tải trung bình.
- Hệ thống hỗ trợ tối thiểu 500 giao dịch trong giờ cao điểm.
- Báo cáo cần được xử lý trong vòng 10 giây.

### 3.2 Tính khả dụng
- Hệ thống hoạt động 99% thời gian trong một năm.
- Có cơ chế backup dữ liệu hàng ngày.
- Khi xảy ra lỗi, hệ thống phải phục hồi nhanh và không làm mất dữ liệu quan trọng.

### 3.3 Bảo mật
- Mật khẩu được mã hóa bằng thuật toán an toàn.
- Dữ liệu thanh toán không lưu thông tin thẻ trực tiếp.
- Chỉ người dùng có quyền mới truy cập chức năng phù hợp.
- Tất cả dữ liệu truyền giữa client và server phải dùng HTTPS.

### 3.4 Khả năng mở rộng
- Hệ thống dễ thêm dịch vụ mới, phương thức thanh toán mới và kênh thông báo mới.
- Kiến trúc phân lớp giúp nâng cấp dễ dàng.

### 3.5 Tính dễ sử dụng
- Giao diện rõ ràng, dễ hiểu và thân thiện với người dùng.
- Màn hình được tối ưu cho desktop và mobile.
- Hệ thống hỗ trợ tiếng Việt cơ bản.

### 3.6 Khả năng bảo trì
- Mã nguồn được tổ chức rõ ràng theo module.
- Có thể kiểm thử và nâng cấp từng phần mà không ảnh hưởng lớn đến hệ thống.

## 4. Ràng buộc nghiệp vụ
- Một khách hàng không thể đặt lịch trùng giờ cho cùng một dịch vụ.
- Mỗi đặt lịch phải có trạng thái rõ ràng.
- Dịch vụ tạm dừng không được phép đặt mới.
- Chỉ quản trị viên có quyền quản lý dịch vụ và phân quyền.
- Chỉ người có quyền mới có thể cập nhật trạng thái đơn.

## 5. Kết luận
Yêu cầu hệ thống tập trung vào việc hỗ trợ khách hàng đặt lịch, thanh toán, theo dõi tiến độ và nhận thông báo, đồng thời hỗ trợ nhân viên và quản trị viên hiệu quả trong quản lý dịch vụ và báo cáo.
