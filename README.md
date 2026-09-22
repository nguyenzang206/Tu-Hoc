# IoT

# Day 1

1. Đọc mạch, lập trình 8 - bit, hàn, in vỏ
2. Ngắt, bus, đa nhiệm, đọc datasheet, vẽ PCB
3. Giao thức, máy chủ, dữ liệu, bảo mật, vận hành
4. Thời gian thực - Edge AL phàn cứng - an toàn
5. Quy trình kiểm thử, chứng nhận, sản xuất

Bốn yêu cầu cơ bản của một hệ IoT
1. địa chỉ duy nhất - mỗi vật một tên: mã node <device_id>
2. cảm nhận và tác động: cảm biến ẩm đất, bơm
3. khả năng giao tiếp: wifi -> broker MQTT
4. thông báo và điều khiển: dashboard, cảnh báo, nút tưới

# Day 2

IoT là việc kết nối các thiết bị vật lý với mạng để chúng có thể thu thập dữ liệu, gửi/ nhận dữ liệu và thực hiện hành động
- Một hệ thống IoT cần có 4 việc cơ bản:
+) Cảm nhận: thiết bị phải biết được mọi thứ xung quanh đang xảy ra chuyện gì
  thiết bị lấy thông tin từ sensor (cảm biến)
+) Gửi dữ liệu: thiết bị gửi "nhiệt độ hiện tại là 30 độ C" qua mạng của hệ thống khác
+) Xử lý: một hệ thống sẽ nhận dữ liệu "Nhiệt độ = 30 độ C" -> sau đó quyết định "Nếu nhiệt độ > 28 độ C" -> bật quạt
+) Hành động: Thiết bị thực hiện quyết định ESP32 -> Relay -> bật quạt

Sensor = cảm biến
- Nó giúp thiết bị "cảm nhận" thế giới bên ngoài:
Ví dụ:
DHT11 -> Nhiệt độ + Độ ẩm
DHT22 -> Nhiệt độ + Độ ẩm
LDR -> Ánh sáng
PIR -> Chuyển động
MQ-2 -> Khí/gas
DS18B20 -> Nhiệt độ
PZEM-004T -> Điện áp, dòng điện, công suất, điện năng

=> sensor không tự quyết định phải làm gì, nó chỉ cung cấp thông tin

ESP32 là vi điều khiển (Microcontroller Unit - MCU) có thể đọc cảm biến, xử lý dữ liệu, điều khiển LED, điều khiển relay, điều khiển motor, kết nối WI-FI, giao tiếp Bluetooth, gửi dữ liệu lên Internet, .....

Bên trong ESP32: sensor -> ESP32 (GPIO, CPU, Memory, Wi-Fi, Bluetooth) -> relay / LED

CPU là nơi thực hiện chương trình "Nếu nhiệt độ > 30 độ C" -> Bật quạt
GPIO là các chân của ESP32 giao tiếp với bên ngoài, có 2 kiểu cơ bản:
+) Input: ESP32 đọc dữ liệu: Button -> GPIO -> ESP32
+) Output: ESP điều khiển: ESP32 -> GPIO -> LED

#Day 3
