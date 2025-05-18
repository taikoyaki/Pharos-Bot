### Bot Tự Động cho Pharos Testnet

Một bot tự động để tương tác với **Pharos Testnet**, thực hiện các thao tác như **hoán đổi (swap)**, **chuyển token (transfer)**, **nhận token từ faucet**, và **điểm danh hàng ngày**, nhằm **tăng khả năng nhận airdrop**.

---

### Tính năng ✨

* **Hoán đổi tự động**: Thực hiện hoán đổi ngẫu nhiên giữa token WPHRS và USDC
* **Chuyển PHRS**: Gửi một lượng nhỏ PHRS đến các địa chỉ ngẫu nhiên
* **Nhận faucet**: Tự động nhận token testnet từ faucet
* **Điểm danh hàng ngày**: Hoàn thành nhiệm vụ điểm danh để có cơ hội nhận phần thưởng
* **Hỗ trợ proxy**: Luân phiên proxy cho mỗi thao tác (nếu có)
* **Hỗ trợ nhiều ví**: Xử lý nhiều ví một cách tuần tự

---

### Yêu cầu 📋

* Node.js (v18 trở lên)
* npm hoặc yarn
* Ví Pharos Testnet với private key
* (Tùy chọn) Danh sách proxy trong tệp `proxies.txt`

---

### Cài đặt ⚙️

1. Clone repository:

   ```bash
   git clone https://github.com/vikitoshi/Pharos-Auto-Bot.git
   cd Pharos-Auto-Bot
   ```

2. Cài đặt thư viện:

   ```bash
   npm install
   ```

3. Tạo file `.env` chứa private key của bạn:

   ```
   PRIVATE_KEY_1=private_key_thu_nhat
   PRIVATE_KEY_2=private_key_thu_hai
   ```

4. (Tùy chọn) Thêm proxy vào `proxies.txt`:

   ```
   http://user:pass@ip:port
   socks5://user:pass@ip:port
   ```

---

### Cấu hình ⚙️

Bạn có thể tùy chỉnh:

* RPC URL trong `networkConfig`
* Địa chỉ hợp đồng trong `tokens`
* Số lượng hoán đổi trong hàm `performSwap`
* Số lượng chuyển khoản trong hàm `transferPHRS`

---

### Cách sử dụng 🚀

Chạy bot:

```bash
node index.js
```

Quy trình:

1. Hiển thị banner thông tin dự án
2. Tải proxy (nếu có)
3. Xử lý từng ví theo thứ tự:

   * Nhận faucet (nếu có)
   * Điểm danh hàng ngày
   * Chuyển 10 lần PHRS
   * Hoán đổi 10 lần token
4. Lặp lại mỗi 30 phút

---

### Ghi log 📝

Bot hiển thị log theo màu sắc:

* ✅ Thành công (xanh lá)
* ⚠️ Cảnh báo (vàng)
* ❌ Lỗi (đỏ)
* 🔄 Đang xử lý (xanh dương)
* ➤ Các bước thực hiện (trắng)

---

### Lưu ý ⚠️

1. Bot chỉ dành cho Testnet
2. Tuyệt đối không dùng private key của Mainnet
3. Bot chạy liên tục cho đến khi dừng thủ công (Ctrl+C)
4. Tất cả giao dịch dùng gas price bằng 0
5. Có độ trễ ngẫu nhiên giữa các thao tác

---

### Hỗ trợ 💬

Gặp lỗi hoặc có câu hỏi? Vui lòng mở issue trên GitHub.

---

### Miễn trừ trách nhiệm ⚠️

Phần mềm được cung cấp "nguyên trạng". Sử dụng có thể tiềm ẩn rủi ro. Nhà phát triển không chịu trách nhiệm cho bất kỳ thiệt hại nào phát sinh.

---

### Giấy phép 📄

Giấy phép MIT – Xem tệp LICENSE để biết chi tiết.

---
