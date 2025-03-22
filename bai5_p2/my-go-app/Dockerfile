# Sử dụng image Go chính thức
FROM golang:1.20

# Đặt thư mục làm việc trong container
WORKDIR /app

# Copy toàn bộ mã nguồn vào thư mục làm việc
COPY . .

# Biên dịch ứng dụng Go
RUN go mod init my-go-app && go mod tidy
RUN go build -o my-go-app

# Mở cổng 8080
EXPOSE 8080

# Chạy ứng dụng
CMD ["/app/my-go-app"]
