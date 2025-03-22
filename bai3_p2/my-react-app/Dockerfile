# Sử dụng node:18-alpine làm base image
FROM node:18-alpine AS build

# Đặt thư mục làm việc bên trong container
WORKDIR /app

# Copy file package.json và package-lock.json vào container
COPY package*.json ./

# Cài đặt dependencies
RUN npm install

# Copy toàn bộ mã nguồn vào container
COPY . .

# Build ứng dụng React
RUN npm run build

# Sử dụng Nginx làm web server để phục vụ ứng dụng React
FROM nginx:stable-alpine AS production

# Copy file build từ bước trước vào thư mục phục vụ web của Nginx
COPY --from=build /app/build /usr/share/nginx/html

# Mở cổng 80
EXPOSE 80

# Chạy Nginx khi container khởi động
CMD ["nginx", "-g", "daemon off;"]
