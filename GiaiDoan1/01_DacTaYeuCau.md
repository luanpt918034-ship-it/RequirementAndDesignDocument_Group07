# Giai đoạn 1 - Đặc tả yêu cầu

## 1. Mục tiêu hệ thống
Hệ thống quản lý đặt lịch và dịch vụ trực tuyến hỗ trợ khách hàng đặt lịch, thanh toán, theo dõi tiến độ và nhận thông báo. Hệ thống cũng hỗ trợ nhân viên và quản trị viên trong quản lý dịch vụ, lịch hẹn và báo cáo.

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
Yêu cầu hệ thống tập trung vào việc hỗ trợ khách hàng đặt lịch, thanh toán, theo dõi tiến độ và nhận thông báo, đồng thời hỗ trợ nhân viên và quản trị viên trong quản lý dịch vụ và báo cáo.

## 6. Yêu cầu chức năng chi tiết và yêu cầu phi chức năng bổ sung

### 1. Yêu cầu chức năng

#### 1.1 Nhóm chức năng chung
| Mã | Chức năng | Mô tả |
|---|---|---|
| FR01 | Đăng nhập | Người dùng đăng nhập bằng tên đăng nhập và mật khẩu; hệ thống xác thực và chuyển đến giao diện theo vai trò |
| FR02 | Đăng xuất | Kết thúc phiên làm việc |
| FR03 | Đổi mật khẩu | Người dùng đổi mật khẩu sau khi nhập đúng mật khẩu cũ |
| FR04 | Quên mật khẩu | Gửi liên kết đặt lại mật khẩu qua email đã đăng ký |
| FR05 | Xem và cập nhật hồ sơ cá nhân | Xem họ tên, mã số, email; cập nhật email, số điện thoại |

#### 1.2 Chức năng của giảng viên
| Mã | Chức năng | Mô tả |
|---|---|---|
| FR06 | Xem danh sách lớp phụ trách | Hiển thị các lớp học phần giảng viên đang dạy trong học kỳ |
| FR07 | Mở phiên điểm danh | Chọn buổi học, đặt thời gian hiệu lực (ví dụ 10 phút) và hệ thống sinh mã QR |
| FR08 | Điểm danh bằng mã QR | Sinh viên quét mã để tự ghi nhận có mặt; hệ thống tự đánh dấu đi muộn nếu quá giờ quy định |
| FR09 | Điểm danh thủ công | Giảng viên đánh dấu trạng thái từng sinh viên trong danh sách lớp |
| FR10 | Đóng phiên điểm danh | Kết thúc phiên; sinh viên chưa điểm danh được đánh dấu Vắng |
| FR11 | Chỉnh sửa kết quả điểm danh | Sửa trạng thái của sinh viên kèm ghi chú lý do; hệ thống lưu lịch sử chỉnh sửa |
| FR12 | Duyệt đơn xin vắng | Chấp nhận hoặc từ chối đơn xin vắng của sinh viên; nếu chấp nhận, trạng thái chuyển thành Có phép |
| FR13 | Xem báo cáo chuyên cần lớp | Xem bảng tổng hợp theo sinh viên và theo buổi; lọc, tìm kiếm |
| FR14 | Xuất báo cáo | Xuất báo cáo chuyên cần ra tệp Excel hoặc PDF |
| FR15 | Cảnh báo vắng quá giới hạn | Hiển thị danh sách sinh viên có số buổi vắng vượt ngưỡng (ví dụ 20% tổng số buổi) |

#### 1.3 Chức năng của sinh viên
| Mã | Chức năng | Mô tả |
|---|---|---|
| FR16 | Xem danh sách lớp đã đăng ký | Hiển thị các lớp học phần sinh viên đang theo học |
| FR17 | Quét mã QR để điểm danh | Gửi mã QR vừa quét lên hệ thống; hệ thống kiểm tra mã còn hiệu lực và sinh viên thuộc lớp |
| FR18 | Xem lịch sử điểm danh | Xem trạng thái từng buổi và tỷ lệ chuyên cần theo từng môn |
| FR19 | Gửi đơn xin vắng | Chọn buổi học, nhập lý do, đính kèm minh chứng (tùy chọn) |
| FR20 | Nhận thông báo | Nhận thông báo kết quả duyệt đơn và cảnh báo vắng nhiều |

#### 1.4 Chức năng của quản trị viên
| Mã | Chức năng | Mô tả |
|---|---|---|
| FR21 | Quản lý tài khoản | Thêm, sửa, khóa, mở khóa, đặt lại mật khẩu cho giảng viên và sinh viên |
| FR22 | Quản lý môn học | Thêm, sửa, xóa môn học |
| FR23 | Quản lý lớp học phần | Tạo lớp, gán giảng viên, nhập danh sách sinh viên (thủ công hoặc nhập từ tệp Excel) |
| FR24 | Quản lý lịch học | Tạo các buổi học theo lịch của lớp học phần |
| FR25 | Cấu hình quy định điểm danh | Thiết lập thời gian hiệu lực mã QR, ngưỡng đi muộn, ngưỡng vắng tối đa |
| FR26 | Thống kê và báo cáo toàn trường | Thống kê theo khoa, môn, lớp; xuất báo cáo |

### 2. Yêu cầu phi chức năng

| Mã | Nhóm | Mô tả | Tiêu chí đo |
|---|---|---|---|
| NFR01 | Hiệu năng | Thao tác điểm danh của sinh viên phải phản hồi nhanh | Phản hồi dưới 2 giây với 200 người dùng đồng thời |
| NFR02 | Hiệu năng | Báo cáo của một lớp được tạo nhanh | Dưới 5 giây cho lớp 100 sinh viên, 15 buổi |
| NFR03 | Bảo mật | Mật khẩu được băm (ví dụ bcrypt), không lưu dạng rõ | Kiểm tra trực tiếp trong cơ sở dữ liệu |
| NFR04 | Bảo mật | Phân quyền theo vai trò; người dùng không truy cập được chức năng ngoài quyền | Kiểm thử phân quyền cho cả 3 vai trò |
| NFR05 | Bảo mật | Mã QR chỉ có hiệu lực trong thời gian ngắn và chỉ dùng cho đúng buổi học; chặn một sinh viên điểm danh nhiều lần | Mã hết hạn sau thời gian cấu hình |
| NFR06 | Bảo mật | Phiên đăng nhập tự hết hạn sau 30 phút không hoạt động | Kiểm thử thủ công |
| NFR07 | Độ tin cậy | Hệ thống hoạt động ổn định trong giờ học; có sao lưu dữ liệu hằng ngày | Khả dụng từ 99% trong giờ hành chính |
| NFR08 | Khả năng sử dụng | Giao diện tiếng Việt, rõ ràng, người dùng mới thực hiện được điểm danh trong tối đa 3 thao tác | Khảo sát thử nghiệm với 5 người dùng |
| NFR09 | Tương thích | Chạy trên trình duyệt Chrome, Edge, Firefox bản mới; giao diện co giãn tốt trên điện thoại | Kiểm thử trên 3 trình duyệt và màn hình 360 px trở lên |
| NFR10 | Bảo trì | Mã nguồn tổ chức theo kiến trúc phân lớp, có chú thích, có kiểm thử đơn vị cho các lớp nghiệp vụ chính | Độ bao phủ kiểm thử từ 60% |
| NFR11 | Toàn vẹn dữ liệu | Mọi chỉnh sửa điểm danh được ghi nhật ký (ai sửa, lúc nào, giá trị cũ và mới) | Bảng nhật ký đầy đủ |
| NFR12 | Triển khai | Đóng gói bằng Docker để triển khai nhanh | Chạy được bằng một lệnh docker compose |

### 3. Ghi chú
Phần này bổ sung chi tiết cho các yêu cầu chức năng và phi chức năng của hệ thống điểm danh, nhằm hỗ trợ quá trình phân tích, thiết kế và kiểm thử phần mềm trong giai đoạn tiếp theo.
