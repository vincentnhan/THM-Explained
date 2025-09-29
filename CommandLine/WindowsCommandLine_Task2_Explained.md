# Windows Command Line – Task 2 (Basic System Information) — Explained v1 (Fixed)

> **Chốt đáp án theo lab:**  
> **OS version:** `10.0.20348.2655`  •  **Hostname:** `WINSRV2022-CORE`  
> (Máy lab đang dùng **Windows Server 2022 Core**, không phải 2019.)

---

## Q1 (THM): What is the OS version of the Windows VM?
- **Đáp án:** `10.0.20348.2655`.  
- **Vì sao đúng:** Theo output chuẩn của máy lab (Windows Server 2022 Core). `ver` và `systeminfo` đều hiển thị đúng build.  
- **Cách tự kiểm chứng:**
```powershell
ver
systeminfo | findstr /B /C:"OS Version"
```
- **Lưu ý:** Con số build có thể thay đổi theo snapshot/lab, nhưng với lab hiện tại là `10.0.20348.2655`.

---

## Q2 (THM): What is the hostname of the Windows VM?
- **Đáp án:** `WINSRV2022-CORE`.  
- **Vì sao đúng:** Phù hợp với hostname hiển thị trong lab. `hostname` và `systeminfo` đều trả về cùng giá trị.  
- **Cách tự kiểm chứng:**
```powershell
hostname
systeminfo | findstr /B /C:"Host Name"
```
- **Lưu ý:** Hostname có thể khác nếu bạn đổi tên máy; dùng lệnh để xác thực thay vì đoán.

---

## Q3 (Bổ sung): Lệnh `set` dùng để làm gì?
- **Đáp án:** Hiển thị toàn bộ environment variables hiện có.  
- **Vì sao đúng:** `set` dump toàn bộ key=value, bao gồm PATH.  
- **Cách tự kiểm chứng:**
```powershell
set | more
```
- **Lưu ý:** Kết quả dài, nên pipe `| more` hoặc chuyển qua PowerShell: `gci Env:`.

---

## Q4 (Bổ sung): Cách xem danh sách driver đã cài bằng CMD?
- **Đáp án:** `driverquery`.  
- **Vì sao đúng:** Lệnh built-in để liệt kê driver, version, date.  
- **Cách tự kiểm chứng:**
```powershell
driverquery | more
```
- **Lưu ý:** Trên Server Core, một số thành phần có thể tối giản; vẫn đọc được danh sách driver.

---

## Q5 (Bổ sung): Lệnh `cls` có tác dụng gì?
- **Đáp án:** Xóa sạch màn hình CMD hiện tại.  
- **Vì sao đúng:** `cls` (clear screen) là tiện ích cơ bản của Windows CMD.  
- **Cách tự kiểm chứng:**
```powershell
cls
```
- **Lưu ý:** Không xóa command history, chỉ xóa phần hiển thị.

---

## Q6 (Bổ sung): Làm sao để xem help cho một lệnh?
- **Đáp án:** `help <command>` hoặc `<command> /?`.  
- **Vì sao đúng:** Cách nhanh để tra cứu syntax trong CMD/Server Core.  
- **Cách tự kiểm chứng:**
```powershell
help systeminfo
systeminfo /?
```
- **Lưu ý:** Một số lệnh chỉ hỗ trợ `/?.` Với PowerShell, dùng `Get-Help <cmdlet>`.