# website_QLDVCVGT
I. Cấu trúc thư mục
/congvien_giaitri/
│
├── /admin/                         # Trang quản trị
│   ├── index.php                   # Dashboard
│   ├── login.php                   # Đăng nhập quản trị
│   ├── logout.php
│   ├── quanly_dichvu.php           # Quản lý dịch vụ
│   ├── quanly_ve.php               # Quản lý vé
│   ├── quanly_nhanvien.php         # Quản lý nhân viên
│   ├── quanly_khachhang.php        # Quản lý khách hàng
│   ├── thongke.php                 # Thống kê
│   ├── /includes/                  # File include dùng chung admin
│   │   ├── header.php
│   │   ├── sidebar.php
│   │   ├── footer.php
│   └── /assets/                    # CSS, JS, ảnh admin
│       ├── css/
│       ├── js/
│       └── images/
│
├── /user/                          # Trang người dùng
│   ├── index.php                   # Trang chủ
│   ├── dichvu.php                  # Danh sách dịch vụ
│   ├── chitiet_dichvu.php          # Chi tiết dịch vụ
│   ├── dat_ve.php                  # Đặt vé
│   ├── lichsu_datve.php            # Lịch sử đặt vé
│   ├── lienhe.php                  # Liên hệ
│   ├── login.php                   # Đăng nhập user
│   ├── register.php                # Đăng ký user
│   ├── profile.php                 # Thông tin cá nhân
│   ├── /templates/                 # Giao diện chung
│   │   ├── header.php
│   │   ├── footer.php
│   │   ├── navbar.php
│   └── /assets/                    # CSS, JS, ảnh user
│       ├── css/
│       ├── js/
│       └── images/
│
├── /includes/                      # File dùng chung cho cả site
│   ├── db_connect.php              # Kết nối DB
│   ├── functions.php               # Hàm tiện ích
│
├── /uploads/                       # Ảnh upload: dịch vụ, avatar...
│
├── /config/                        # File cấu hình
│   └── config.php
│
└── index.php                       # Trang chuyển hướng chính (home)
II. Luồng hoạt động
Luồng chạy của website
🔹 1. Người dùng (User)
Truy cập trang chủ (index.php)
Đăng ký / đăng nhập (register.php / login.php)
Xem danh sách dịch vụ (dichvu.php)
→ Xem chi tiết dịch vụ (chitiet_dichvu.php)
Đặt vé (dat_ve.php)
→ Chọn số lượng, phương thức thanh toán
Lịch sử đặt vé (lichsu_datve.php)
Hiển thị vé đã đặt, phân loại: chờ xácnhận, đã thanh toán, đã hủy
Quản lý thông tin cá nhân (profile.php)
Gửi phản hồi (lienhe.php)
🔹 2. Quản trị (Admin)
Đăng nhập (login.php) → Dashboard (index.php)
Quản lý:
Dịch vụ (quanly_dichvu.php)
Vé (quanly_ve.php) → xác nhận thanh toán / hủy vé
Nhân viên (quanly_nhanvien.php)
Khách hàng (quanly_khachhang.php)
Xem thống kê doanh thu, số vé (thongke.php)
🔹 3. Mối quan hệ chính
nguoi_dung ↔ ve ↔ dich_vu
nguoi_dung ↔ phan_hoi
Admin quản lý ve, dich_vu, nguoi_dung, nhan_vien, thong_ke
