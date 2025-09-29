# Windows Command Line – Task 6 (Conclusion) — Explained v1

---

## Q1 (THM): What is the command you can use to restart a system?
- **Đáp án:** `shutdown /r`  
- **Vì sao đúng:** `/r` (restart) là option chuẩn của `shutdown`. Lệnh sẽ khởi động lại máy thay vì tắt hẳn.  
- **Cách tự kiểm chứng:**
```powershell
shutdown /r /t 0
```
- **Lưu ý:** `/t 0` để thực hiện ngay lập tức, nếu không Windows sẽ đếm ngược.

---

## Q2 (THM): What command can you use to abort a scheduled system shutdown?
- **Đáp án:** `shutdown /a`  
- **Vì sao đúng:** `/a` (abort) hủy lệnh shutdown/restart đã lên lịch.  
- **Cách tự kiểm chứng:**
```powershell
shutdown /s /t 60
shutdown /a
```
- **Lưu ý:** Chỉ có tác dụng trong khi Windows đang đếm ngược tắt máy.

---

## Q3 (Bổ sung): Lệnh `chkdsk` dùng để làm gì?
- **Đáp án:** Kiểm tra và sửa lỗi hệ thống tập tin, bad sector trên ổ đĩa.  
- **Vì sao đúng:** `chkdsk` là công cụ chuẩn để kiểm tra file system.  
- **Cách tự kiểm chứng:**
```powershell
chkdsk C:
```
- **Lưu ý:** Có thể cần `/f` hoặc `/r` để sửa lỗi, và phải chạy với quyền Admin.

---

## Q4 (Bổ sung): Lệnh `sfc /scannow` dùng khi nào?
- **Đáp án:** Dùng để quét và sửa file hệ thống bị lỗi/corrupt.  
- **Vì sao đúng:** `sfc` = System File Checker, có khả năng tự động replace file lỗi từ cache.  
- **Cách tự kiểm chứng:**
```powershell
sfc /scannow
```
- **Lưu ý:** Thường mất vài phút, log được ghi tại `C:\Windows\Logs\CBS\CBS.log`.

---

## Q5 (Bổ sung): `driverquery` có tác dụng gì?
- **Đáp án:** Liệt kê tất cả driver đã cài.  
- **Vì sao đúng:** Hữu ích khi kiểm tra sự cố driver, phiên bản.  
- **Cách tự kiểm chứng:**
```powershell
driverquery | more
```
- **Lưu ý:** Có thể thêm `/v` để hiển thị chi tiết hơn (date, path).

---

## Q6 (Bổ sung): Lệnh `more` dùng trong những trường hợp nào?
- **Đáp án:** Xem file text hoặc phân trang output dài.  
- **Vì sao đúng:** `more` giúp đọc nội dung theo trang, tránh tràn màn hình.  
- **Cách tự kiểm chứng:**
```powershell
more readme.txt
systeminfo | more
```
- **Lưu ý:** Với PowerShell có thể thay thế bằng `Out-Host -Paging`.

---

✅ Task 6 đã được giải thích theo format: **Đáp án → Vì sao đúng → Cách tự kiểm chứng → Lưu ý** (2 câu THM + 4 câu bổ sung).