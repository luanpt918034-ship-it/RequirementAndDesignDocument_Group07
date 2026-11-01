# Giai đoạn 1 - Đặc tả yêu cầu

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
