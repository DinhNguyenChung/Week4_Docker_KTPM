# Sử dụng image Nginx mới nhất
FROM nginx:latest

# Copy file index.html vào thư mục gốc của Nginx
COPY index.html /usr/share/nginx/html/

# Mở cổng 80
EXPOSE 80

# Chạy Nginx
CMD ["nginx", "-g", "daemon off;"]
