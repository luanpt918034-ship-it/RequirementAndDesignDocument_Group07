# Giai đoạn 1 - Sơ đồ lớp (Class Diagram)

## 1. Sơ đồ lớp
```mermaid
classDiagram
    class User {
        +userId: String
        +fullName: String
        +email: String
        +phone: String
        +password: String
        +role: String
    }

    class Customer {
        +makeBooking()
        +cancelBooking()
        +pay()
    }

    class Staff {
        +viewAssignedBookings()
        +updateBookingStatus()
    }

    class Admin {
        +manageUsers()
        +manageServices()
        +viewReports()
    }

    class Service {
        +serviceId: String
        +name: String
        +description: String
        +price: Double
        +duration: Integer
        +status: String
    }

    class Booking {
        +bookingId: String
        +bookingDate: Date
        +startTime: Time
        +status: String
        +totalPrice: Double
    }

    class Payment {
        +paymentId: String
        +amount: Double
        +paymentMethod: String
        +status: String
        +transactionCode: String
    }

    class Notification {
        +notificationId: String
        +message: String
        +notifyType: String
        +sendTime: DateTime
    }

    class Report {
        +reportId: String
        +date: Date
        +revenue: Double
        +summary: String
    }

    User <|-- Customer
    User <|-- Staff
    User <|-- Admin

    Customer "1" --> "0..*" Booking
    Service "1" --> "0..*" Booking
    Booking "1" --> "0..1" Payment
    Booking "1" --> "0..*" Notification
    Admin "1" --> "0..*" Report
    Staff "1" --> "0..*" Booking
```

## 2. Mô tả các lớp chính
- User: lưu thông tin người dùng, phân quyền.
- Customer: khách hàng, thực hiện đặt lịch và thanh toán.
- Staff: nhân viên, xử lý lịch hẹn và cập nhật trạng thái.
- Admin: quản trị viên, quản lý tài nguyên hệ thống.
- Service: mô tả thông tin dịch vụ.
- Booking: đơn đặt lịch.
- Payment: thanh toán cho đơn đặt lịch.
- Notification: thông báo và nhắc lịch.
- Report: báo cáo thống kê.

## 3. Kết luận
Sơ đồ lớp cho thấy mối quan hệ giữa các thực thể trong hệ thống và là nền tảng cho việc thiết kế cơ sở dữ liệu và mã nguồn trong các giai đoạn tiếp theo.
