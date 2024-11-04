# เริ่มจากใช้ Node image เป็นฐาน
FROM node:16-alpine

# กำหนด working directory ใน container
WORKDIR /app

# คัดลอกไฟล์ package.json และ package-lock.json
COPY package*.json ./

# ติดตั้ง dependencies
RUN npm install

# คัดลอกไฟล์โปรเจคทั้งหมดไปยัง container
COPY . .

# สร้างไฟล์ production build
RUN npm run build

# ระบุพอร์ตที่จะใช้
EXPOSE 3000

# คำสั่งสำหรับเริ่มเซิร์ฟเวอร์
CMD ["npm", "run", "start"]
