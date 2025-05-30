# Hệ Thống Quản Lý Phòng Cấy Mô

Hệ thống quản lý phòng cấy mô được xây dựng bằng MERN Stack (MongoDB, Express, React, Node.js).

## Tính Năng

- Quản lý mẫu cấy
  - Thêm, sửa, xóa mẫu cấy
  - Theo dõi trạng thái mẫu
  - Quản lý vị trí lưu trữ
  - Lịch sử thay đổi

- Quản lý người dùng
  - Phân quyền (Admin, Quản lý, Nhân viên)
  - Đăng nhập/Đăng xuất
  - Quản lý thông tin cá nhân

- Báo cáo và thống kê
  - Theo dõi tình trạng mẫu
  - Thống kê theo thời gian
  - Xuất báo cáo

## Cài Đặt

### Yêu Cầu

- Node.js
- MongoDB
- npm hoặc yarn

### Backend

```bash
# Di chuyển vào thư mục server
cd server

# Cài đặt dependencies
npm install

# Tạo file .env và cấu hình
cp .env.example .env

# Khởi động server
npm run dev
```

### Frontend

```bash
# Di chuyển vào thư mục client
cd client

# Cài đặt dependencies
npm install

# Khởi động ứng dụng
npm start
```

## Cấu Trúc Dự Án

```
quan-ly-cay-mo/
├── server/             # Backend
│   ├── models/         # MongoDB models
│   ├── routes/         # API routes
│   ├── middleware/     # Middleware
│   └── index.js        # Entry point
│
└── client/            # Frontend (sẽ được tạo sau)
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── services/
    │   └── App.tsx
    └── package.json
```

## API Endpoints

### Mẫu Cấy
- `GET /api/mau-cay` - Lấy danh sách mẫu cấy
- `POST /api/mau-cay` - Tạo mẫu cấy mới
- `GET /api/mau-cay/:id` - Xem chi tiết mẫu cấy
- `PUT /api/mau-cay/:id` - Cập nhật mẫu cấy
- `GET /api/mau-cay/:id/lich-su` - Xem lịch sử mẫu cấy

### Người Dùng
- `POST /api/nguoi-dung/dang-nhap` - Đăng nhập
- `POST /api/nguoi-dung` - Tạo người dùng mới
- `GET /api/nguoi-dung` - Lấy danh sách người dùng
- `PUT /api/nguoi-dung/:id` - Cập nhật thông tin người dùng
- `POST /api/nguoi-dung/doi-mat-khau` - Đổi mật khẩu

## Tác Giả

[Tên của bạn]

## Giấy Phép

MIT 