# Chính Sách Bảo Mật và Báo Cáo Lỗi

## Báo Cáo Lỗ Hổng Bảo Mật

Nếu bạn phát hiện bất kỳ lỗ hổng bảo mật nào trong NK-DL, vui lòng báo cáo cho chúng tôi một cách có trách nhiệm. **Không công khai lỗ hổng trước khi chúng tôi có cơ hội sửa chữa.**

### Cách Báo Cáo
1. Gửi email đến: tuilanomoka@gmail.com
2. Tiêu đề: "[NK-DL SECURITY] Mô tả ngắn về vấn đề"
3. Bao gồm:
   - Mô tả chi tiết về lỗ hổng
   - Các bước để tái tạo vấn đề
   - Môi trường và phiên bản bị ảnh hưởng
   - Bất kỳ tác động tiềm ẩn nào

Chúng tôi sẽ phản hồi trong vòng 48 giờ và cập nhật tiến trình sửa lỗi.

## Các Biện Pháp Bảo Mật Hiện Tại

### 1. Xử Lý Dữ Liệu Người Dùng
- Không thu thập hoặc lưu trữ dữ liệu cá nhân
- Mọi video tải về đều được xóa khỏi server sau 1 giờ
- Không sử dụng database hoặc lưu trữ lâu dài

### 2. Bảo Mật Ứng Dụng Web
- Giới hạn tỷ lệ yêu cầu (rate limiting) để ngăn chặn tấn công DDoS
- Xác thực đầu vào người dùng để tránh injection
- Sử dụng Flask với các cài đặt bảo mật mặc định

### 3. Phụ Thuộc Bên Thứ Ba
- Thường xuyên cập nhật dependencies
- Chỉ sử dụng các thư viện đáng tin cậy từ PyPI
- Kiểm tra các lỗ hổng đã biết trong dependencies

## Các Biện Pháp Bảo Mật Được Khuyến Nghị Khi Triển Khai

### Triển Khai Trên Máy Chủ Riêng
1. **Luôn sử dụng HTTPS** với chứng chỉ SSL hợp lệ
2. **Cấu hình tường lửa** để chỉ mở các cổng cần thiết
3. **Cập nhật hệ điều hành** và các gói phần mềm thường xuyên
4. **Sử dụng môi trường ảo hóa** để cô lập ứng dụng
5. **Thiết lập sao lưu định kỳ** cho cấu hình

### Triển Khai Cục Bộ
1. **Không chạy với quyền root** trên hệ thống
2. **Sử dụng virtual environment** cho Python
3. **Giới hạn quyền truy cập** vào thư mục ứng dụng
4. **Theo dõi nhật ký** để phát hiện hoạt động đáng ngờ

## Phạm Vi Chịu Trách Nhiệm

### Chúng Tôi Chịu Trách Nhiệm
- Bảo mật mã nguồn của NK-DL
- Sửa chữa các lỗ hổng bảo mật trong mã nguồn
- Cung cấp bản cập nhật bảo mật

### Chúng Tôi KHÔNG Chịu Trách Nhiệm
- Bảo mật của máy chủ triển khai
- Cấu hình sai từ phía người dùng
- Các lỗ hổng trong các thư viện bên thứ ba
- Việc sử dụng sai mục đích của công cụ

## Liên Hệ
Mọi vấn đề về bảo mật, vui lòng liên hệ qua:
- GitHub Issues (cho vấn đề không nhạy cảm)
- Email trực tiếp (cho vấn đề nhạy cảm)

---
*Lưu ý: Đây là dự án mã nguồn mở và không có bảo đảm về bảo mật. Người dùng tự chịu trách nhiệm khi triển khai.*