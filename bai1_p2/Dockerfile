# Sử dụng Node.js 18 làm base image
FROM node:18

# Thiết lập thư mục làm việc bên trong container
WORKDIR /app

# Sao chép các file vào container
COPY package*.json ./
RUN npm install

COPY . .

# Mở cổng 3000
EXPOSE 3000

# Chạy ứng dụng
CMD ["node", "server.js"]
