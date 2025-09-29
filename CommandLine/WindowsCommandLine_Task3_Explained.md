# Windows Command Line – Task 3 (Network Troubleshooting) — Explained v1

---

## Q1 (THM): Which command can we use to look up the server’s physical address (MAC address)?
- **Đáp án:** `ipconfig /all`  
- **Vì sao đúng:** Lệnh này hiển thị chi tiết network adapter, bao gồm Physical Address (MAC).  
- **Cách tự kiểm chứng:**
```powershell
ipconfig /all
```
- **Lưu ý:** MAC address hiển thị dạng `XX-XX-XX-XX-XX-XX` và duy nhất cho mỗi card mạng.

---

## Q2 (THM): What is the name of the service listening on port 135?
- **Đáp án:** `RpcSs`  
- **Vì sao đúng:** Netstat với option `-abon` cho thấy service RpcSs (Remote Procedure Call) lắng nghe cổng 135.  
- **Cách tự kiểm chứng:**
```powershell
netstat -abon | findstr 135
```
- **Lưu ý:** Port 135 là cổng chuẩn cho RPC Endpoint Mapper.

---

## Q3 (THM): What is the name of the service listening on port 3389?
- **Đáp án:** `TermService`  
- **Vì sao đúng:** Netstat xác nhận dịch vụ TermService (Remote Desktop Services) lắng nghe cổng 3389.  
- **Cách tự kiểm chứng:**
```powershell
netstat -abon | findstr 3389
```
- **Lưu ý:** Đây là cổng mặc định cho RDP (Remote Desktop Protocol).

---

## Q4 (Bổ sung): Lệnh `ping` dùng để làm gì?
- **Đáp án:** Gửi ICMP echo request để kiểm tra khả năng reach đến host.  
- **Vì sao đúng:** Nếu có reply, chứng tỏ kết nối tới host hoạt động.  
- **Cách tự kiểm chứng:**
```powershell
ping example.com
```
- **Lưu ý:** Một số firewall có thể block ICMP, không phản hồi dù host vẫn online.

---

## Q5 (Bổ sung): `tracert` khác gì `ping`?
- **Đáp án:** `tracert` hiển thị tuyến đường (hops) đến host, trong khi `ping` chỉ kiểm tra reachability.  
- **Vì sao đúng:** Tracert lợi dụng TTL để hiển thị từng router trên đường đi.  
- **Cách tự kiểm chứng:**
```powershell
tracert example.com
```
- **Lưu ý:** Kết quả có thể thay đổi tùy mạng, một số hop có thể timeout.

---

## Q6 (Bổ sung): `nslookup` dùng để làm gì?
- **Đáp án:** Tra cứu DNS để lấy IP của tên miền.  
- **Vì sao đúng:** Đây là công cụ built-in DNS query.  
- **Cách tự kiểm chứng:**
```powershell
nslookup example.com
```
- **Lưu ý:** Có thể chỉ định DNS server cụ thể: `nslookup example.com 1.1.1.1`.

---

## Q7 (Bổ sung): Lệnh `netstat -abon` có ý nghĩa gì?
- **Đáp án:** Liệt kê kết nối mạng + port lắng nghe + process name + PID.  
- **Vì sao đúng:** Các option `-a` (all), `-b` (process), `-o` (PID), `-n` (numeric).  
- **Cách tự kiểm chứng:**
```powershell
netstat -abon
```
- **Lưu ý:** Cần chạy CMD với quyền Admin để thấy đủ thông tin.