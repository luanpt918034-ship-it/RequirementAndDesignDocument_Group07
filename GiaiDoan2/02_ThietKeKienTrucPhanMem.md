# Giai đoạn 2 - Thiết kế kiến trúc phần mềm

## 1. Mục tiêu kiến trúc
Kiến trúc phần mềm cần đảm bảo tính phân tách rõ ràng giữa giao diện, logic nghiệp vụ, dữ liệu và giao tiếp với bên ngoài. Từ đó giúp hệ thống dễ mở rộng, bảo trì và tích hợp.

## 2. Kiến trúc đề xuất
### 2.1 Kiến trúc 3 lớp
```text
+----------------------+ 
| Presentation Layer   |  Frontend / GUI
| - Login             |
| - Dashboard         |
| - Booking           |
| - Payment           |
+----------------------+
          |
          v
+----------------------+ 
| Application Layer   |  Business logic / API
| - UserService       |
| - BookingService    |
| - PaymentService    |
| - ReportService     |
+----------------------+
          |
          v
+----------------------+ 
| Data Layer          |  Database + storage
| - User             |
| - Service          |
| - Booking          |
| - Payment          |
| - Notification     |
+----------------------+
```

## 3. Các thành phần chính
- Frontend: giao diện người dùng web/app.
- API Backend: xử lý nghiệp vụ, xác thực quyền, gọi database.
- Database: lưu dữ liệu người dùng, lịch hẹn, dịch vụ, thanh toán.
- Notification Service: gửi email/SMS/nhắc lịch.
- Payment Gateway: tích hợp cổng thanh toán.

## 4. Lợi ích của kiến trúc
- Tách biệt rõ ràng chức năng và dữ liệu.
- Dễ nâng cấp từng module riêng biệt.
- Hỗ trợ phát triển theo nhóm.
- Dễ tích hợp thêm dịch vụ mới.

## 5. Kiến trúc triển khai đề xuất
- Frontend: React / Angular / Vue
- Backend: Node.js / Spring Boot / ASP.NET
- Database: MySQL / PostgreSQL
- Deployment: Docker + CI/CD + cloud hosting

## 6. Kết luận
Thiết kế kiến trúc phần mềm theo mô hình 3 lớp giúp hệ thống rõ ràng, dễ mở rộng và phù hợp cho hệ thống quản lý đặt lịch trong thực tế.
