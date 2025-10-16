# 🎯 คู่มือสร้างไฟล์ .mind สำหรับ AR Marker

## 📋 ขั้นตอนการสร้างไฟล์ .mind

### 1️⃣ เตรียมรูป Marker
คุณมีรูป marker อยู่ในโฟลเดอร์ `images` แล้ว:
- P1.png (สำหรับ targetIndex: 0)
- P2.png (สำหรับ targetIndex: 1) 
- P3.png (สำหรับ targetIndex: 2)
- P4.png (สำหรับ targetIndex: 3)
- P5.png (สำหรับ targetIndex: 4)
- P6.png (สำหรับ targetIndex: 5)
- P7.png (สำหรับ targetIndex: 6)
- P8.png (สำหรับ targetIndex: 7)
- P9.png (สำหรับ targetIndex: 8)
- P10.png (สำหรับ targetIndex: 9)

### 2️⃣ ใช้ MindAR Compiler
เว็บไซต์ที่เปิดไว้ให้: https://hiukim.github.io/mind-ar-js-doc/tools/compile

**ขั้นตอน:**
1. คลิก "Select Image Files"
2. เลือกไฟล์ P1.png ถึง P10.png จากโฟลเดอร์ images (เลือกทีละไฟล์หรือหลายไฟล์พร้อมกัน)
3. คลิก "Start Compile"
4. รอให้ระบบประมวลผล (ใช้เวลาประมาณ 1-2 นาที)
5. เมื่อเสร็จแล้วจะมีปุ่ม "Download" ให้คลิก
6. ดาวน์โหลดไฟล์ "targets.mind"

### 3️⃣ ติดตั้งไฟล์ .mind ใหม่
1. เปลี่ยนชื่อไฟล์ที่ดาวน์โหลดมาจาก "targets.mind" เป็น "targets1.mind"
2. ย้ายไฟล์ไปใส่ในโฟลเดอร์ `markers` (แทนที่ไฟล์เก่า)

### 4️⃣ ปรับโค้ด scanner.html
ไฟล์ .mind ใหม่จะมี targetIndex ดังนี้:
- targetIndex: 0 = P1.png
- targetIndex: 1 = P2.png  
- targetIndex: 2 = P3.png
- targetIndex: 3 = P4.png
- targetIndex: 4 = P5.png
- targetIndex: 5 = P6.png
- targetIndex: 6 = P7.png
- targetIndex: 7 = P8.png
- targetIndex: 8 = P9.png
- targetIndex: 9 = P10.png

## 🎮 การใช้งาน
1. เปิดไฟล์ scanner.html
2. อนุญาตให้เข้าถึงกล้อง
3. นำกล้องส่องที่รูป P1.png ถึง P10.png
4. โมเดล 3D จะปรากฏขึ้นตาม targetIndex ที่กำหนดไว้

## ⚠️ หมายเหตุ
- รูป marker ต้องพิมพ์ออกมาหรือแสดงบนหน้าจอให้ชัดเจน
- ขนาดรูปควรใหญ่พอที่กล้องจะจับได้
- แสงไฟต้องเพียงพอ ไม่เบลอ

## 🔧 หากมีปัญหา
- ตรวจสอบไฟล์ targets1.mind ในโฟลเดอร์ markers
- ตรวจสอบ targetIndex ในโค้ด scanner.html ให้ตรงกับรูป marker
- ลองเปลี่ยนขนาดรูป marker หรือปรับแสง