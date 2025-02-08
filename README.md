README - Phân tích Kết quả Kiểm thử Hiệu suất với JMeter

1. Giới thiệu

Tài liệu này phân tích kết quả kiểm thử hiệu suất của hệ thống web bằng Apache JMeter. Hai kịch bản kiểm thử đã được thực hiện:

Test Plan50: Kiểm thử với 50 người dùng đồng thời.

Test Plan100: Kiểm thử với 100 người dùng đồng thời.

2. Thiết lập Kiểm thử

Thời gian kiểm thử: 5 phút.

Ramp-up Time: 10 giây.

Loại kiểm thử:

Kiểm thử tải (Load Testing): Ghi nhận thời gian phản hồi và tỷ lệ lỗi.

Kiểm thử khả năng chịu tải (Stress Testing): Xác định giới hạn hệ thống.

3. Phân tích Kết quả

3.1. Kết quả từ Test Plan50 (50 Users)
![50](https://github.com/user-attachments/assets/0b190819-ce44-4ddf-b381-081b16b30a98)

Thời gian phản hồi trung bình: 392

Throughput: 4.9/sec

Tỷ lệ lỗi (Error Rate): 0.00%

Nhận xét: Hệ thống có thể xử lý 50 người dùng mà không gặp vấn đề lớn.

3.2. Kết quả từ Test Plan100 (100 Users)
![100](https://github.com/user-attachments/assets/dcd4be9c-d02a-4160-9a05-cb4ae07712a5)

Thời gian phản hồi trung bình: 453

Throughput: 9.7/sec

Tỷ lệ lỗi (Error Rate): 0.00%

Nhận xét: Khi tăng lên 100 người dùng, hiệu suất hệ thống bắt đầu giảm, có thể xuất hiện bottleneck.

4. Kết luận

Hệ thống hoạt động ổn định ở mức 50 người dùng.

Ở 100 người dùng, có dấu hiệu giảm hiệu suất, cần tối ưu hóa để cải thiện khả năng chịu tải.

5.Câu hỏi thảo luận:
1. **Tại sao kiểm thử phi chức năng quan trọng?**  
   Kiểm thử phi chức năng đảm bảo phần mềm đáp ứng yêu cầu về hiệu suất, bảo mật, khả năng mở rộng và trải nghiệm người dùng, giúp hệ thống hoạt động ổn định trong môi trường thực tế.  

2. **Các thông số quan trọng trong kiểm thử hiệu suất:**  
   - **Thời gian phản hồi (Response Time)**  
   - **Throughput (Lưu lượng yêu cầu/giây)**  
   - **Tỷ lệ lỗi (Error Rate)**  
   - **Sử dụng tài nguyên (CPU, RAM, I/O)**  
   - **Khả năng mở rộng (Scalability)**  

3. **Giải pháp khi hệ thống không đáp ứng yêu cầu hiệu suất:**  
   - **Tối ưu hóa mã nguồn và truy vấn CSDL**  
   - **Cải thiện caching và nén dữ liệu**  
   - **Nâng cấp hạ tầng (CPU, RAM, Load Balancer)**  
   - **Sử dụng CDN và tối ưu mạng**  
   - **Kiểm tra và tinh chỉnh cấu hình server**
