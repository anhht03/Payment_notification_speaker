# Payment_notification_speaker

## 🔊 Giới thiệu dự án
- Dự án Loa thông báo chuyển khoản tự động với ESP32 được xây dựng nhằm hỗ trợ các cửa hàng, quán cà phê, tiệm tạp hóa hoặc cá nhân kinh doanh online dễ dàng nhận biết khi có khách chuyển khoản thanh toán.
Hệ thống hoạt động dựa trên việc nhận dữ liệu giao dịch qua Wi-Fi và phát âm thanh thông báo số tiền, tên người gửi qua loa.
- Nhờ đó, người bán không cần kiểm tra điện thoại liên tục, vẫn có thể biết ngay khi có giao dịch mới, giúp tăng tính tiện lợi, giảm sai sót và nâng cao trải nghiệm bán hàng.

## ⚙️ Tính năng chính
- ✅ Tự động phát thông báo khi có chuyển khoản mới.  
- 💬 Hỗ trợ phát **giọng nói** hoặc **âm báo tùy chỉnh**.  
- 🌐 Kết nối **Wi-Fi** để nhận dữ liệu từ server hoặc API.  
- 🔊 Sử dụng **loa** để phát tín hiệu.  
- ⚡ Có thể chạy độc lập bằng ESP32 hoặc ESP8266.

## 🧠 Nguyên lý hoạt động
1. ESP32 kết nối Wi-Fi và truy cập API của **Sepay** để lấy danh sách giao dịch mới.  
2. Khi phát hiện có **chuyển khoản mới**, ESP32 xử lý dữ liệu và:  
   - Phát âm thanh hoặc giọng nói thông báo nội dung (ví dụ: *"Bạn vừa nhận 500.000 đồng từ Nguyễn Văn A"*)  
   - Hiển thị thông tin trên màn hình OLED.  
3. Sau khi thông báo xong, hệ thống tiếp tục chờ giao dịch tiếp theo.

## 🚀 Cách hoạt động
1. Cập nhật thông tin Wi-Fi và API Key Sepay trong config.h.
2. Nạp code vào ESP32.
3. Khi có giao dịch mới → ESP32 nhận dữ liệu → Phát âm thanh thông báo + hiển thị trên OLED.
