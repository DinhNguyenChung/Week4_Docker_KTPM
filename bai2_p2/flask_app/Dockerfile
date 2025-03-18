# Sử dụng Python 3.9 làm base image
FROM python:3.9

# Đặt thư mục làm việc bên trong container
WORKDIR /app

# Copy toàn bộ code vào container
COPY . /app

# Cài đặt thư viện trong requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Mở cổng 5000
EXPOSE 5000

# Chạy ứng dụng Flask
CMD ["python", "app.py"]
