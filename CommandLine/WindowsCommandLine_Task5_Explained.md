# Windows Command Line – Task 5 (Task and Process Management) — Explained v1

---

## Q1 (THM): What command would you use to find the running processes related to notepad.exe?
- **Đáp án:** `tasklist /FI "imagename eq notepad.exe"`  
- **Vì sao đúng:** `tasklist` liệt kê tất cả process, với option `/FI` để filter theo điều kiện. Ở đây, filter là image name bằng notepad.exe.  
- **Cách tự kiểm chứng:**
```powershell
tasklist /FI "imagename eq notepad.exe"
```
- **Lưu ý:** Có thể thay notepad.exe bằng tên process khác, ví dụ chrome.exe.

---

## Q2 (THM): What command can you use to kill the process with PID 1516?
- **Đáp án:** `taskkill /PID 1516`  
- **Vì sao đúng:** `taskkill` dùng để chấm dứt process theo PID.  
- **Cách tự kiểm chứng:**
```powershell
taskkill /PID 1516
```
- **Lưu ý:** Nếu cần kill nhiều process cùng lúc, có thể dùng `/PID <id1> /PID <id2>` hoặc kill theo tên image: `taskkill /IM notepad.exe /F`.

---

## Q3 (Bổ sung): Làm sao xem toàn bộ process đang chạy?
- **Đáp án:** `tasklist`  
- **Vì sao đúng:** Lệnh hiển thị toàn bộ danh sách process, PID, session, memory usage.  
- **Cách tự kiểm chứng:**
```powershell
tasklist
```
- **Lưu ý:** Output dài, nên dùng `| more` hoặc filter.

---

## Q4 (Bổ sung): Có thể kill process theo tên thay vì PID không?
- **Đáp án:** Có, dùng `taskkill /IM <process_name>`.  
- **Vì sao đúng:** `/IM` cho phép chỉ định image name (vd: notepad.exe).  
- **Cách tự kiểm chứng:**
```powershell
taskkill /IM notepad.exe /F
```
- **Lưu ý:** `/F` để force kill, nếu không có thể fail khi process không phản hồi.

---

## Q5 (Bổ sung): Có thể hiển thị thông tin DLL mà process load không?
- **Đáp án:** `tasklist /M`  
- **Vì sao đúng:** Option `/M` cho phép liệt kê module (DLL) được load bởi process.  
- **Cách tự kiểm chứng:**
```powershell
tasklist /M
```
- **Lưu ý:** Có thể combine: `tasklist /FI "imagename eq notepad.exe" /M`.

---

## Q6 (Bổ sung): Cách lọc process theo user?
- **Đáp án:** `tasklist /FI "username eq <user>"`  
- **Vì sao đúng:** Cho phép xem process thuộc về user cụ thể.  
- **Cách tự kiểm chứng:**
```powershell
tasklist /FI "username eq SYSTEM"
```
- **Lưu ý:** Hữu ích khi phân tích process chạy dưới tài khoản nào.
