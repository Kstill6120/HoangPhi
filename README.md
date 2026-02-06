# 🚗 Hệ Thống Quản Lý Bán Xe Ô Tô VinFast
## Car Sales Management System

<div align="center">

![.NET Framework](https://img.shields.io/badge/.NET%20Framework-4.8-512BD4?style=for-the-badge&logo=.net)
![ASP.NET MVC](https://img.shields.io/badge/ASP.NET-MVC%205-5C2D91?style=for-the-badge&logo=.net)
![SQL Server](https://img.shields.io/badge/SQL%20Server-2019+-CC2927?style=for-the-badge&logo=microsoft-sql-server)
![Entity Framework](https://img.shields.io/badge/Entity%20Framework-6.2.0-512BD4?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)

**Đồ Án Công Nghệ Phần Mềm - Nhóm 5**

[Tính năng](#-tính-năng) • [Công nghệ](#-công-nghệ-sử-dụng) • [Cài đặt](#-hướng-dẫn-cài-đặt) • [Sử dụng](#-hướng-dẫn-sử-dụng) • [Nhóm phát triển](#-thành-viên-nhóm)

</div>

---

## 📋 Mục Lục

- [Giới thiệu](#-giới-thiệu)
- [Tính năng](#-tính-năng)
- [Công nghệ sử dụng](#-công-nghệ-sử-dụng)
- [Kiến trúc hệ thống](#-kiến-trúc-hệ-thống)
- [Hướng dẫn cài đặt](#-hướng-dẫn-cài-đặt)
- [Hướng dẫn sử dụng](#-hướng-dẫn-sử-dụng)
- [Cấu trúc dự án](#-cấu-trúc-dự-án)
- [Thành viên nhóm](#-thành-viên-nhóm)
- [Giấy phép](#-giấy-phép)

---

## 🎯 Giới Thiệu

**Hệ Thống Quản Lý Bán Xe Ô Tô VinFast** là một ứng dụng web quản lý và kinh doanh xe ô tô trực tuyến được phát triển bởi Nhóm 5 trong khuôn khổ môn học Công Nghệ Phần Mềm. Hệ thống cung cấp giải pháp toàn diện cho việc quản lý showroom xe hơi, từ quản lý sản phẩm, khách hàng đến xử lý đơn hàng.

### 🎓 Thông Tin Đồ Án

- **Môn học:** Công Nghệ Phần Mềm (Software Engineering)
- **Nhóm:** Nhóm 5
- **Năm học:** 2024-2025
- **Đề tài:** Hệ Thống Quản Lý Bán Xe Ô Tô

---

## ✨ Tính Năng

### 🔐 Quản Lý Người Dùng & Xác Thực
- ✅ Đăng ký, đăng nhập, đăng xuất
- ✅ Phân quyền người dùng (Admin/Customer)
- ✅ Quản lý thông tin tài khoản cá nhân
- ✅ Bảo mật mật khẩu (Hashing)

### 🚘 Quản Lý Sản Phẩm Xe
- ✅ Xem danh sách xe với thông tin chi tiết
- ✅ Tìm kiếm và lọc xe theo:
  - Hãng xe (VinFast)
  - Khoảng giá
  - Năm sản xuất
  - Từ khóa
- ✅ Xem thông tin chi tiết từng xe
- ✅ Hiển thị hình ảnh và video sản phẩm

### 🛒 Quản Lý Đơn Hàng
- ✅ Thêm xe vào giỏ hàng
- ✅ Đặt hàng trực tuyến
- ✅ Theo dõi trạng thái đơn hàng
- ✅ Lịch sử mua hàng
- ✅ Xác nhận và xử lý đơn hàng (Admin)

### 👥 Quản Lý Khách Hàng
- ✅ Quản lý thông tin khách hàng
- ✅ Theo dõi lịch sử giao dịch
- ✅ Phản hồi và đánh giá sản phẩm

### 📊 Trang Quản Trị (Admin)
- ✅ Dashboard tổng quan
- ✅ Quản lý danh sách xe (CRUD)
- ✅ Quản lý đơn hàng
- ✅ Quản lý khách hàng
- ✅ Nhật ký kiểm toán (Audit Log)
- ✅ Báo cáo thống kê

### 📱 Giao Diện Người Dùng
- ✅ Responsive Design
- ✅ Giao diện hiện đại, thân thiện
- ✅ Tối ưu trải nghiệm người dùng
- ✅ Tích hợp Bootstrap 5

---

## 🛠 Công Nghệ Sử Dụng

### Backend
- **Framework:** ASP.NET MVC 5
- **Runtime:** .NET Framework 4.8
- **ORM:** Entity Framework 6.2.0
- **Language:** C# 8.0

### Frontend
- **HTML5, CSS3, JavaScript**
- **Bootstrap 5** - Responsive UI Framework
- **jQuery** - DOM Manipulation
- **Font Awesome** - Icons

### Database
- **SQL Server 2019+**
- **Database Name:** CARSALE_DB
- **ORM:** Entity Framework (Database First)

### Architecture & Design Patterns
- **MVC (Model-View-Controller)**
- **Repository Pattern**
- **Dependency Injection**
- **Entity Framework Database First**

### Additional Libraries
- **Newtonsoft.Json 13.0.3** - JSON Serialization
- **Microsoft.AspNet.Razor 5.3.0**
- **jQuery 3.7.1**
- **Bootstrap 5.3.0**

---

## 🏗 Kiến Trúc Hệ Thống

### Mô Hình MVC

```
┌─────────────────────────────────────────────────────────┐
│                        Client                            │
│                    (Web Browser)                         │
└───────────────────┬─────────────────────────────────────┘
                    │
                    │ HTTP Request/Response
                    │
┌───────────────────▼─────────────────────────────────────┐
│                    Controllers                           │
│  ┌──────────┬──────────┬──────────┬──────────────────┐  │
│  │  Home    │ Product  │  Order   │  Admin/Account   │  │
│  └──────────┴──────────┴──────────┴──────────────────┘  │
└───────────────────┬─────────────────────────────────────┘
                    │
                    │ Business Logic
                    │
┌───────────────────▼─────────────────────────────────────┐
│                    Models & Data                         │
│  ┌──────────────────────────────────────────────────┐   │
│  │  Repository Layer (Data Access)                  │   │
│  │  - CarRepository                                 │   │
│  │  - CustomerRepository                            │   │
│  │  - OrderRepository                               │   │
│  │  - AuditRepository                               │   │
│  └──────────────────┬───────────────────────────────┘   │
│                     │                                    │
│  ┌──────────────────▼───────────────────────────────┐   │
│  │  Entity Framework (ORM)                          │   │
│  └──────────────────┬───────────────────────────────┘   │
└─────────────────────┼─────────────────────────────────┬─┘
                      │                                 │
                      │ SQL Queries                     │
                      │                                 │
┌─────────────────────▼─────────────────────────────────▼─┐
│                   SQL Server Database                    │
│                      CARSALE_DB                          │
└──────────────────────────────────────────────────────────┘
```

### Database Schema

```
CARSALE_DB
├── CAR                 (Thông tin xe)
├── CUSTOMER            (Thông tin khách hàng)
├── ORDER               (Đơn hàng)
├── ORDER_DETAIL        (Chi tiết đơn hàng)
├── ACCOUNT_ROLE        (Phân quyền tài khoản)
├── FEEDBACK            (Phản hồi khách hàng)
└── AUDIT_LOG           (Nhật ký hệ thống)
```

---

## 📥 Hướng Dẫn Cài Đặt

### Yêu Cầu Hệ Thống

#### Phần Mềm Bắt Buộc
- **Windows 10/11** hoặc **Windows Server 2019+**
- **Visual Studio 2019/2022** (Community, Professional hoặc Enterprise)
  - Workload: ASP.NET and web development
- **SQL Server 2019+** (Express, Developer hoặc Standard)
- **SQL Server Management Studio (SSMS)** 18.0+
- **.NET Framework 4.8 SDK**

#### Phần Mềm Khuyến Nghị
- **IIS 10.0+** (để deploy production)
- **Git** (để quản lý source code)

### Các Bước Cài Đặt

#### 1️⃣ Clone Repository

```bash
git clone https://github.com/HoaiNam2k5/DA_CNPM_GROUP_5.git
cd DA_CNPM_GROUP_5
```

#### 2️⃣ Cấu Hình Database

**Bước 1:** Mở SQL Server Management Studio (SSMS)

**Bước 2:** Chạy script tạo database

```sql
-- Chạy file: Database/CarSaleScrip.sql
-- Hoặc: Database/Carsale.sql
```

**Bước 3:** Kiểm tra database đã được tạo

```sql
USE CARSALE_DB;
GO

-- Kiểm tra các bảng
SELECT * FROM INFORMATION_SCHEMA.TABLES;
```

#### 3️⃣ Cấu Hình Connection String

Mở file `WebCar/WebCar/Web.config` và cập nhật connection string:

```xml
<connectionStrings>
  <add name="CARSALE_DBEntities" 
       connectionString="metadata=res://*/Models.Model1.csdl|res://*/Models.Model1.ssdl|res://*/Models.Model1.msl;
       provider=System.Data.SqlClient;
       provider connection string=&quot;
       data source=YOUR_SERVER_NAME;
       initial catalog=CARSALE_DB;
       integrated security=True;
       encrypt=False;
       trustservercertificate=True;
       MultipleActiveResultSets=True;
       App=EntityFramework&quot;" 
       providerName="System.Data.EntityClient" />
</connectionStrings>
```

**Lưu ý:** Thay `YOUR_SERVER_NAME` bằng tên SQL Server của bạn. Ví dụ:
- `localhost` hoặc `.` (local machine)
- `localhost\SQLEXPRESS` (SQL Server Express)
- `(localdb)\MSSQLLocalDB` (LocalDB)

#### 4️⃣ Mở Solution trong Visual Studio

**Bước 1:** Mở Visual Studio

**Bước 2:** Mở solution file

```
File → Open → Project/Solution
Chọn: WebCar/WebCar.sln
```

**Bước 3:** Restore NuGet Packages

```
Tools → NuGet Package Manager → Manage NuGet Packages for Solution
Click "Restore" nếu có thông báo
```

Hoặc sử dụng Package Manager Console:

```powershell
Update-Package -reinstall
```

#### 5️⃣ Build Solution

```
Build → Build Solution (Ctrl + Shift + B)
```

Đảm bảo build thành công không có lỗi.

#### 6️⃣ Chạy Ứng Dụng

**Cách 1:** Debug trong Visual Studio
```
Debug → Start Debugging (F5)
hoặc
Debug → Start Without Debugging (Ctrl + F5)
```

Ứng dụng sẽ tự động mở trên trình duyệt tại: `https://localhost:44312/`

---

## 📖 Hướng Dẫn Sử Dụng

### Tài Khoản Mặc Định

#### Admin Account
```
Username: admin
Password: admin123
Role: Administrator
```

#### Customer Account
```
Username: customer01
Password: customer123
Role: Customer
```

### Quy Trình Sử Dụng

#### 👤 Đối với Khách Hàng

1. **Đăng ký tài khoản**
   - Truy cập: `/Account/Register`
   - Điền thông tin cá nhân
   - Xác nhận đăng ký

2. **Đăng nhập**
   - Truy cập: `/Account/Login`
   - Nhập username và password
   - Click "Đăng nhập"

3. **Tìm kiếm và xem xe**
   - Truy cập: `/Product/Index`
   - Sử dụng bộ lọc tìm kiếm
   - Click vào xe để xem chi tiết

4. **Đặt hàng**
   - Chọn xe muốn mua
   - Click "Đặt hàng"
   - Điền thông tin giao hàng
   - Xác nhận đơn hàng

5. **Theo dõi đơn hàng**
   - Truy cập: `/Order/MyOrders`
   - Xem trạng thái đơn hàng
   - Xem chi tiết đơn hàng

#### 👨‍💼 Đối với Admin

1. **Truy cập trang quản trị**
   - Đăng nhập bằng tài khoản Admin
   - Truy cập: `/Admin/Dashboard`

2. **Quản lý xe**
   - Truy cập: `/Admin/Cars`
   - Thêm/Sửa/Xóa thông tin xe
   - Upload hình ảnh và video

3. **Quản lý đơn hàng**
   - Truy cập: `/Admin/Orders`
   - Xem danh sách đơn hàng
   - Cập nhật trạng thái đơn hàng
   - Xác nhận/Hủy đơn hàng

4. **Quản lý khách hàng**
   - Truy cập: `/Admin/Customers`
   - Xem thông tin khách hàng
   - Quản lý tài khoản

5. **Xem nhật ký hệ thống**
   - Truy cập: `/Audit/Index`
   - Xem lịch sử thay đổi
   - Theo dõi hoạt động người dùng

---

## 📁 Cấu Trúc Dự Án

```
DA_CNPM_GROUP_5/
│
├── Database/                          # Database Scripts
│   ├── CarSaleScrip.sql              # Main database schema
│   └── Carsale.sql                   # Alternative schema
│
├── WebCar/                           # Main Application
│   ├── WebCar.sln                    # Visual Studio Solution
│   │
│   └── WebCar/                       # Web Project
│       ├── App_Start/                # Application Configuration
│       │   ├── BundleConfig.cs       # CSS/JS bundles
│       │   ├── FilterConfig.cs       # Action filters
│       │   └── RouteConfig.cs        # URL routing
│       │
│       ├── Controllers/              # MVC Controllers
│       │   ├── AccountController.cs  # Authentication & User Management
│       │   ├── AdminController.cs    # Admin Dashboard
│       │   ├── AuditController.cs    # Audit Logs
│       │   ├── HomeController.cs     # Home & Static Pages
│       │   ├── OrderController.cs    # Order Management
│       │   └── ProductController.cs  # Product/Car Management
│       │
│       ├── Data/                     # Data Access Layer (Repository Pattern)
│       │   ├── AuditRepository.cs    # Audit log operations
│       │   ├── CarRepository.cs      # Car CRUD operations
│       │   ├── CustomerRepository.cs # Customer management
│       │   └── OrderRepository.cs    # Order processing
│       │
│       ├── Models/                   # Data Models (Entity Framework)
│       │   ├── ACCOUNT_ROLE.cs       # User roles
│       │   ├── AUDIT_LOG.cs          # Audit log model
│       │   ├── CAR.cs                # Car entity
│       │   ├── CUSTOMER.cs           # Customer entity
│       │   ├── FEEDBACK.cs           # Feedback model
│       │   ├── ORDER.cs              # Order entity
│       │   ├── ORDER_DETAIL.cs       # Order details
│       │   ├── Model1.cs             # EF DbContext
│       │   └── ViewModels/           # View-specific models
│       │
│       ├── Views/                    # Razor Views
│       │   ├── Account/              # Login, Register views
│       │   ├── Admin/                # Admin panel views
│       │   ├── Audit/                # Audit log views
│       │   ├── Home/                 # Home page views
│       │   ├── Order/                # Order views
│       │   ├── Product/              # Product/Car views
│       │   ├── Shared/               # Shared layouts & partials
│       │   │   ├── _Layout.cshtml    # Main layout
│       │   │   └── _AdminLayout.cshtml # Admin layout
│       │   └── Web.config
│       │
│       ├── Content/                  # CSS Styles
│       │   ├── bootstrap.css
│       │   └── Site.css              # Custom styles
│       │
│       ├── Scripts/                  # JavaScript Files
│       │   ├── jquery-3.7.1.js
│       │   ├── bootstrap.js
│       │   └── custom scripts
│       │
│       ├── images/                   # Car Images
│       │   ├── vinfast_vf3.jpg
│       │   ├── vinfast_vf6.jpg
│       │   ├── vinfast_vf8_eco.jpg
│       │   └── ...
│       │
│       ├── video/                    # Video Content
│       │
│       ├── Filters/                  # Custom Action Filters
│       │   └── AuthorizeRoleAttribute.cs # Role-based authorization
│       │
│       ├── Web.config                # Application Configuration
│       ├── packages.config           # NuGet Packages
│       └── Global.asax.cs            # Application Entry Point
│
├── .vs/                              # Visual Studio Settings
├── .git/                             # Git Repository
│
└── README.md                         # This file
```

---

## 👥 Thành Viên Nhóm

<div align="center">

| STT | Họ và Tên | GitHub | Vai Trò |
|-----|-----------|--------|---------|
| 1 | **Hoài Nam** | [@HoaiNam2k5](https://github.com/HoaiNam2k5) | Team Leader, Full-stack Developer |
| - | _Các thành viên khác_ | - | _Đang cập nhật..._ |

</div>

---

## 🤝 Đóng Góp

Chúng tôi rất hoan nghênh mọi đóng góp cho dự án! Nếu bạn muốn đóng góp:

1. Fork dự án
2. Tạo branch mới (`git checkout -b feature/AmazingFeature`)
3. Commit thay đổi (`git commit -m 'Add some AmazingFeature'`)
4. Push lên branch (`git push origin feature/AmazingFeature`)
5. Tạo Pull Request

---

## 📝 Changelog

### Version 1.0.0 (Current)
- ✅ Hoàn thành chức năng quản lý xe
- ✅ Hoàn thành chức năng đặt hàng
- ✅ Hoàn thành trang quản trị Admin
- ✅ Tích hợp Audit Log
- ✅ Responsive UI

---

## 🐛 Báo Lỗi

Nếu bạn phát hiện lỗi hoặc có đề xuất tính năng mới, vui lòng:
1. Tạo [Issue](https://github.com/HoaiNam2k5/DA_CNPM_GROUP_5/issues) mới
2. Mô tả chi tiết vấn đề
3. Đính kèm screenshots nếu có

---

## 📞 Liên Hệ

- **GitHub:** [@HoaiNam2k5](https://github.com/HoaiNam2k5)
- **Repository:** [https://github.com/HoaiNam2k5/DA_CNPM_GROUP_5](https://github.com/HoaiNam2k5/DA_CNPM_GROUP_5)
- **Issues:** [Report Issues](https://github.com/HoaiNam2k5/DA_CNPM_GROUP_5/issues)

---

## 📄 Giấy Phép

Dự án này được phát triển cho mục đích học tập trong khuôn khổ môn Công Nghệ Phần Mềm.

```
MIT License

Copyright (c) 2024 Nhóm 5 - DA_CNPM_GROUP_5

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🌟 Acknowledgments

- Cảm ơn **Giảng viên** môn Công Nghệ Phần Mềm đã hướng dẫn
- Cảm ơn **VinFast** đã cung cấp hình ảnh minh họa
- Cảm ơn **Bootstrap Team** cho framework tuyệt vời
- Cảm ơn **Microsoft** cho .NET Framework và Entity Framework

---

<div align="center">

### ⭐ Nếu bạn thấy dự án hữu ích, hãy cho chúng tôi một Star! ⭐

**Made with ❤️ by Nhóm 5**

</div>

