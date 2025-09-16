# 🚗 Car Rental System

ระบบจองรถเช่าออนไลน์ที่พัฒนาด้วย React, Node.js และ MongoDB พร้อมฟีเจอร์ครบครันสำหรับผู้ใช้งานทั่วไปและเจ้าของรถ

## 📋 สารบัญ
- [ฟีเจอร์หลัก](#-ฟีเจอร์หลัก)
- [เทคโนโลยีที่ใช้](#-เทคโนโลยีที่ใช้)
- [การติดตั้ง](#-การติดตั้ง)
- [การใช้งาน](#-การใช้งาน)
- [โครงสร้างโปรเจค](#-โครงสร้างโปรเจค)
- [API Endpoints](#-api-endpoints)
- [Screenshots](#-screenshots)
- [เครดิต](#-เครดิต)

## ✨ ฟีเจอร์หลัก

### สำหรับผู้ใช้งาน (User)
- 🔐 ระบบสมัครสมาชิก/เข้าสู่ระบบ
- 🔍 ค้นหารถตามสถานที่และวันที่
- 📅 ตรวจสอบความพร้อมใช้งานของรถ
- 💳 จองรถและชำระเงิน
- 📊 ดูประวัติการจองของตนเอง
- 📱 Responsive Design สำหรับทุกอุปกรณ์

### สำหรับเจ้าของรถ (Owner)
- 🚙 เพิ่มรถเข่าใหม่พร้อมรูปภาพ
- ⚙️ จัดการรถของตนเอง (เปิด/ปิด การใช้งาน, ลบ)
- 📈 Dashboard แสดงสถิติการจอง
- 💰 ติดตามรายได้รายเดือน
- 📋 จัดการสถานะการจอง (อนุมัติ/ยกเลิก)
- 👤 อัพเดทโปรไฟล์และรูปภาพ

### ฟีเจอร์เพิ่มเติม
- 🎨 UI/UX ที่สวยงามด้วย Motion Animations
- 🌐 รองรับหลายสถานที่
- 📊 ระบบกรองและค้นหาขั้นสูง
- 🔄 Real-time อัพเดทข้อมูล

## 🛠 เทคโนโลยีที่ใช้

### Frontend
- **React 19** - JavaScript Library
- **React Router Dom** - สำหรับการจัดการ Route
- **Motion** - สำหรับ Animation
- **Tailwind CSS 4** - CSS Framework
- **Axios** - HTTP Client
- **React Hot Toast** - Notification

### Backend
- **Node.js** - Runtime Environment
- **Express.js** - Web Framework
- **MongoDB** - NoSQL Database
- **Mongoose** - MongoDB ODM
- **JWT** - Authentication
- **Bcrypt** - Password Hashing
- **ImageKit** - Image Storage & Optimization
- **Multer** - File Upload

## 📦 การติดตั้ง

### ข้อกำหนดเบื้องต้น
- Node.js (v18 หรือสูงกว่า)
- MongoDB
- ImageKit Account
- Git

### 1. Clone โปรเจค
```bash
git clone https://github.com/your-username/car-rental-system.git
cd car-rental-system
```

### 2. ติดตั้ง Dependencies

#### สำหรับ Server
```bash
cd server
npm install
```

#### สำหรับ Client
```bash
cd client
npm install
```

### 3. ตั้งค่า Environment Variables

#### สำหรับ Server (server/.env)
```env
MONGODB_URI=mongodb://localhost:27017
JWT_SECRET=your_jwt_secret_key
IMAGEKIT_PUBLIC_KEY=your_imagekit_public_key
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
IMAGEKIT_URL_ENDPOINT=your_imagekit_url_endpoint
PORT=5000
```

#### สำหรับ Client (client/.env)
```env
VITE_BASE_URL=http://localhost:5000
VITE_CURRENCY=$
```

### 4. เริ่มต้นการพัฒนา

#### เริ่ม Server
```bash
cd server
npm run server
```

#### เริ่ม Client
```bash
cd client
npm run dev
```

แอปพลิเคชันจะทำงานที่:
- Frontend: http://localhost:5173
- Backend: http://localhost:5000

## 🎯 การใช้งาน

### สำหรับผู้ใช้งานใหม่
1. **สมัครสมาชิก** - สร้างบัญชีใหม่
2. **ค้นหารถ** - เลือกสถานที่และวันที่ที่ต้องการ
3. **เลือกรถ** - ดูรายละเอียดและจองรถ
4. **ติดตามการจอง** - ตรวจสอบสถานะในหน้า "My Bookings"

### สำหรับเจ้าของรถ
1. **เปลี่ยนบทบาท** - คลิก "List cars" เพื่อเป็น Owner
2. **เพิ่มรถ** - อัพโหลดรูปและกรอกรายละเอียด
3. **จัดการ** - เปิด/ปิดการใช้งาน หรือลบรถ
4. **อนุมัติการจอง** - จัดการคำขอจองจาก Dashboard

## 📁 โครงสร้างโปรเจค

```
car-rental-system/
├── client/                 # React Frontend
│   ├── src/
│   │   ├── components/     # React Components
│   │   ├── pages/          # หน้าต่างๆ
│   │   ├── context/        # Context API
│   │   ├── assets/         # ไฟล์ static
│   │   └── main.jsx        # Entry point
│   ├── public/
│   └── package.json
├── server/                 # Node.js Backend
│   ├── controllers/        # Business Logic
│   ├── models/             # Database Models
│   ├── routes/             # API Routes
│   ├── middleware/         # Middleware functions
│   ├── configs/            # Configuration files
│   └── server.js           # Entry point
└── README.md
```

## 🔌 API Endpoints

### Authentication
- `POST /api/user/register` - สมัครสมาชิก
- `POST /api/user/login` - เข้าสู่ระบบ
- `GET /api/user/data` - ข้อมูลผู้ใช้

### Cars
- `GET /api/user/cars` - ดูรถทั้งหมด
- `POST /api/owner/add-car` - เพิ่มรถใหม่
- `GET /api/owner/cars` - รถของ Owner
- `POST /api/owner/toggle-car` - เปิด/ปิดการใช้งาน
- `POST /api/owner/delete-car` - ลบรถ

### Bookings
- `POST /api/bookings/check-availability` - ตรวจสอบความพร้อมใช้งาน
- `POST /api/bookings/create` - สร้างการจอง
- `GET /api/bookings/user` - การจองของผู้ใช้
- `GET /api/bookings/owner` - การจองของ Owner
- `POST /api/bookings/change-status` - เปลี่ยนสถานะการจอง

### Owner
- `POST /api/owner/change-role` - เปลี่ยนเป็น Owner
- `GET /api/owner/dashboard` - ข้อมูล Dashboard
- `POST /api/owner/update-image` - อัพเดทรูปโปรไฟล์

## 📱 Screenshots

### หน้าแรก (Home)
- Hero Section พร้อมฟอร์มค้นหา
- Featured Cars Section
- Banner สำหรับ Owner
- Testimonials และ Newsletter

### หน้ารถทั้งหมด (Cars)
- ระบบกรองและค้นหา
- แสดงรถในรูปแบบ Card
- ข้อมูลรถที่ครบถ้วน

### หน้ารายละเอียดรถ (Car Details)
- รูปภาพรถขนาดใหญ่
- ข้อมูลรถที่สมบูรณ์
- ฟอร์มจองรถ

### Dashboard Owner
- สถิติการจองและรายได้
- จัดการรถและการจอง
- อัพเดทข้อมูลส่วนตัว

## 🚀 Deployment

### Frontend (Vercel)
```bash
cd client
npm run build
# Deploy ผ่าน Vercel CLI หรือ GitHub integration
```

### Backend (Vercel/Railway)
```bash
cd server
# ตั้งค่า Environment Variables
# Deploy ผ่าน platform ที่เลือก
```

## 🤝 การมีส่วนร่วม

1. Fork โปรเจค
2. สร้าง Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit การเปลี่ยนแปลง (`git commit -m 'Add some AmazingFeature'`)
4. Push ไปยัง Branch (`git push origin feature/AmazingFeature`)
5. เปิด Pull Request



## 🙏 เครดิต

โปรเจคนี้พัฒนาโดยอ้างอิงจาก Tutorial:
**[Car Rental Website Tutorial](https://youtu.be/tBObk72EYYw?si=h7jp5Jc7W7GeQ_16)**

ขอบคุณสำหรับการแบ่งปันความรู้และแนวทางในการพัฒนาระบบ Car Rental ที่สมบูรณ์


