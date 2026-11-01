# Giai đoạn 1 - Sơ đồ DFD

## 1. DFD mức 0
```mermaid
flowchart LR
    A[Khách hàng] -->|Đặt lịch / xem dịch vụ| B[Hệ thống quản lý đặt lịch]
    C[Nhân viên] -->|Xử lý đơn / cập nhật trạng thái| B
    D[Quản trị viên] -->|Quản lý dịch vụ / báo cáo| B
    E[Cổng thanh toán] -->|Xác nhận thanh toán| B
    B -->|Thông báo / lịch hẹn| A
    B -->|Báo cáo| D
    B --> F[(CSDL)]
```

## 2. DFD mức 1
```mermaid
flowchart TD
    A[Khách hàng] --> P1[Quản lý tài khoản]
    A --> P2[Quản lý đặt lịch]
    A --> P3[Quản lý thanh toán]

    C[Nhân viên] --> P2
    C --> P4[Quản lý xử lý đơn]

    D[Quản trị viên] --> P5[Quản lý dịch vụ]
    D --> P6[Quản lý báo cáo]

    P1 --> DB[(CSDL)]
    P2 --> DB
    P3 --> DB
    P4 --> DB
    P5 --> DB
    P6 --> DB

    P3 --> E[Cổng thanh toán]
    P2 --> N[Thông báo / nhắc lịch]
    N --> A
```

## 3. Giải thích luồng dữ liệu
- Khách hàng gửi yêu cầu đăng nhập, xem dịch vụ, đặt lịch và thanh toán.
- Hệ thống lưu trữ dữ liệu vào CSDL và gửi thông báo lại cho người dùng.
- Nhân viên cập nhật trạng thái đơn và ghi nhận kết quả xử lý.
- Quản trị viên quản lý dữ liệu dịch vụ và báo cáo doanh thu.
