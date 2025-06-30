# 🎮 Space Invader on STM32F429ZiT6

Project cuối kỳ phát triển trò chơi Space Invader trên vi điều khiển STM32F429ZiT6 sử dụng FreeRTOS và TouchGFX.

## 📋 Mục lục

- [Giới thiệu](#giới-thiệu)
- [Yêu cầu hệ thống](#yêu-cầu-hệ-thống)
- [Cài đặt môi trường](#cài-đặt-môi-trường)
  - [STM32CubeIDE](#1-cài-đặt-stm32cubeide)
  - [TouchGFX Designer](#2-cài-đặt-touchgfx-designer)
  - [Các công cụ hỗ trợ khác](#3-các-công-cụ-hỗ-trợ-khác)
- [Cách build và chạy project](#cách-build-và-chạy-project)
- [Đóng góp](#đóng-góp)

---

## 🎯 Giới thiệu

Đây là project game **Space Invader** được cài đặt trực tiếp trên board **STM32F429ZiT6 Discovery Kit**, sử dụng hệ điều hành **FreeRTOS** và giao diện hiển thị được thiết kế bằng **TouchGFX**. Người chơi điều khiển tàu không gian để tiêu diệt các kẻ thù xuất hiện trên màn hình.

---

## 💻 Yêu cầu hệ thống

- Windows 10 64-bit / Ubuntu 20.04+
- RAM: Tối thiểu 8GB
- Dung lượng trống: 5GB+
- Java Runtime (nếu TouchGFX yêu cầu)

---

## 🛠️ Cài đặt môi trường

### 1. Cài đặt STM32CubeIDE

> STM32CubeIDE là môi trường phát triển tích hợp (IDE) để lập trình và nạp code cho STM32.

**Bước thực hiện:**

1. Truy cập: [https://www.st.com/en/development-tools/stm32cubeide.html](https://www.st.com/en/development-tools/stm32cubeide.html)
2. Tải về và cài đặt phiên bản phù hợp với hệ điều hành.
3. Mở IDE, cập nhật các gói liên quan đến **STM32F4 Series** nếu được yêu cầu.

> 🔖 Phiên bản khuyến nghị: **STM32CubeIDE v1.14.0** trở lên.

---

### 2. Cài đặt TouchGFX Designer

> TouchGFX là công cụ thiết kế giao diện người dùng cho STM32 có màn hình LCD.

**Bước thực hiện:**

1. Truy cập: [https://www.st.com/en/development-tools/touchgfx.html](https://www.st.com/en/development-tools/touchgfx.html)
2. Tải và cài đặt TouchGFX Designer.
3. Mở TouchGFX Designer → chọn board: `STM32F429I-DISC1`.
4. Tạo hoặc mở project TouchGFX từ thư mục project.

> 🔖 Phiên bản khuyến nghị: **TouchGFX 4.23.0** hoặc mới hơn.

---
### 3. Các công cụ hỗ trợ khác
---

## 🚀 Cách build và chạy project

### 1. Clone project về máy

Sử dụng Git để tải source code từ GitHub:

```bash
git clone https://github.com/KumaMichio/Space_Invader_Embedded.git
```

#### Mô tả các module chính  

- `main.c`: khởi tạo hệ thống, start scheduler  
- `game.c/.h`: quản lý trạng thái game  
- `player.c/.h`: điều khiển tàu người chơi  
- `enemy.c/.h`: xử lý kẻ địch  
- `graphics.c/.h`: giao tiếp với TouchGFX  
- `sound.c/.h`: phát âm thanh đơn giản  
- `FreeRTOSConfig.h`: cấu hình hệ điều hành  

#### Đóng góp của từng thành viên  

| Tên thành viên    | Đóng góp chính | Số commit |
|-------------------|----------------|------------|
| Phan Sỹ Hùng      | Logic game, enemy |          |
| Hoàng Đức Cường   | TouchGFX UI, joystick |          |
| Nguyễn Trọng Hinh | FreeRTOS, sound, README |          |
