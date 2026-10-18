# Phần 1. Phân tích hệ thống Smart-Farm

**Input / Output:**

-   **Input:** Dữ liệu thô từ cảm biến độ ẩm đất, nhiệt độ không khí, độ ẩm không khí.
-   **Output:** Lệnh điều khiển rơ-le bật/tắt máy bơm, dữ liệu log lưu vào `farm_data.csv`, cảnh báo gửi về điện thoại.

**Sơ đồ phối hợp phần cứng:**  
`Cảm biến (DHT22 + Soil Moisture) -> Vi điều khiển ESP32 -> CPU Server xử lý -> Module Relay -> Máy bơm`

# Phần 2. File README.md hoàn chỉnh

# 🚀 Smart-Farm - Trang trại Lan

## 1. Mô tả
Hệ thống ***tưới lan thông minh*** giúp *tiết kiệm nước* và **tự động 100%**, hoạt động 24/7.

## 2. Sơ đồ hệ thống
![So do he thong Smart Farm - ESP32 ket noi cam bien do am va may bom tuoi lan - Alt Text phong khi loi mang](https://rikkeiedu-storage.s3.ap-southeast-2.amazonaws.com/uploads/editor-images/1787648283613_687ec2e7-229c-4942-a347-080fae59560a.webp)


# Phần 3. Kiểm thử

## Xử lý khi RAM đầy

> **CẢNH BÁO:** Khi RAM đầy do file `logs/farm.log` quá lớn, hệ thống có thể bị treo.

**Cách xử lý an toàn - TUYỆT ĐỐI không rút nguồn:**

1.  Dừng tạm hệ thống: `Ctrl + C`
2.  Chạy lệnh dọn dẹp an toàn:
```bash
python clear_log.py
```
