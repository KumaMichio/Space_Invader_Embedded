# Space_Invader_Embedded

- **Biểu đồ luồng (flowchart):**  
- Luồng chính: đọc input → xử lý logic → cập nhật LCD → chờ delay  
- Các task chạy song song dưới FreeRTOS với độ ưu tiên riêng  

---

### **3. Cài đặt / Xây dựng hệ thống**

#### 3.1 Github & hướng dẫn cài đặt  

- Dự án được upload tại: [https://github.com/tenuser/space-invader-stm32](#)  
- File `README.md` có hướng dẫn:  
+ Cài đặt STM32CubeIDE, TouchGFX Designer  
+ Toolchain: STM32Cube_FW_F4, FreeRTOS 10.x  
+ Hướng dẫn build và flash firmware  

#### 3.2 Mô tả các module chính  

- `main.c`: khởi tạo hệ thống, start scheduler  
- `game.c/.h`: quản lý trạng thái game  
- `player.c/.h`: điều khiển tàu người chơi  
- `enemy.c/.h`: xử lý kẻ địch  
- `graphics.c/.h`: giao tiếp với TouchGFX  
- `sound.c/.h`: phát âm thanh đơn giản  
- `FreeRTOSConfig.h`: cấu hình hệ điều hành  

#### 3.3 Đóng góp của từng thành viên  

| Tên thành viên | Đóng góp chính | Số commit |
|----------------|----------------|------------|
| A              | Logic game, enemy | 40         |
| B              | TouchGFX UI, joystick | 35         |
| C              | FreeRTOS, sound, README | 30         |

#### 3.4 Kết quả  

- Game chạy ổn định trên board thật.  
- Có thể điều khiển mượt bằng joystick.  
- Giao diện hiển thị đẹp và rõ ràng.  
- Có video demo quá trình chơi game: [Video Link](#)

#### 3.5 Đánh giá  

- **Đạt được:**  
+ Đáp ứng đầy đủ yêu cầu chức năng và phi chức năng.  
+ Giao diện đẹp, game chơi được, cấu trúc rõ ràng.  

- **Ưu điểm:**  
+ Áp dụng tốt FreeRTOS  
+ Phân chia module hợp lý  
+ Dễ mở rộng (có thể thêm nhiều cấp độ, hiệu ứng âm thanh)  

- **Nhược điểm:**  
+ Đồ họa còn đơn giản  
+ Không có lưu điểm cao  

---

Nếu em cần **bản Word, Markdown, hoặc trình bày slide**, cứ nói em nhé.
