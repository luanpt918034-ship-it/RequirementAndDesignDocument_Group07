# Giai đoạn 1 - Sơ đồ Use Case

## 1. Biểu đồ Use Case
```mermaid
flowchart LR
    actor KhachHang[Khách hàng]
    actor NhanVien[Nhân viên]
    actor QuanTri[Quản trị viên]
    actor ThanhToan[Cổng thanh toán]

    subgraph Hethong[Hệ thống]
        UC1[Đăng ký tài khoản]
        UC2[Đăng nhập]
        UC3[Xem dịch vụ]
        UC4[Đặt lịch]
        UC5[Thanh toán]
        UC6[Theo dõi lịch hẹn]
        UC7[Hủy / đổi lịch]
        UC8[Xem đơn được giao]
        UC9[Cập nhật trạng thái]
        UC10[Quản lý dịch vụ]
        UC11[Xem báo cáo]
        UC12[Quản lý tài khoản]
    end

    KhachHang --> UC1
    KhachHang --> UC2
    KhachHang --> UC3
    KhachHang --> UC4
    KhachHang --> UC5
    KhachHang --> UC6
    KhachHang --> UC7

    NhanVien --> UC8
    NhanVien --> UC9

    QuanTri --> UC10
    QuanTri --> UC11
    QuanTri --> UC12

    ThanhToan --> UC5
```

## 2. Mô tả các Use Case chính
- UC1: Đăng ký tài khoản
- UC2: Đăng nhập
- UC3: Xem dịch vụ
- UC4: Đặt lịch
- UC5: Thanh toán
- UC6: Theo dõi lịch hẹn
- UC8: Xem đơn được giao
- UC9: Cập nhật trạng thái đơn
- UC10: Quản lý dịch vụ
- UC11: Xem báo cáo doanh thu
- UC12: Quản lý người dùng và phân quyền

## 3. Kết luận
Sơ đồ Use Case mô tả rõ vai trò của từng actor và các chức năng chính tương ứng trong hệ thống.
