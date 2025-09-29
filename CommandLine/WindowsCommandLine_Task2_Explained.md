# Windows Command Line – Task 2 (Basic System Information) — Explained v1

---

## Q1 (THM): What is the OS version of the Windows VM?
- **Đáp án:** `10.0.17763` (ví dụ theo output: Microsoft Windows [Version 10.0.17763.1821]).  
- **Vì sao đúng:** Lệnh `ver` và `systeminfo` đều hiển thị thông tin OS Version.  
- **Cách tự kiểm chứng:**  
```powershell
ver
systeminfo | findstr /B /C:"OS Version"
```
- **Lưu ý:** Kết quả có thể khác nhau tùy bản build Windows.

---

## Q2 (THM): What is the hostname of the Windows VM?
- **Đáp án:** `WIN-SRV-2019` (theo ví dụ trong output).  
- **Vì sao đúng:** `systeminfo` hiển thị trường *Host Name*.  
- **Cách tự kiểm chứng:**  
```powershell
hostname
systeminfo | findstr /B /C:"Host Name"
```
- **Lưu ý:** Hostname có thể khác tùy máy, không phải lúc nào cũng là WIN-SRV-2019.

---

## Q3 (Bổ sung): Lệnh `set` dùng để làm gì?
- **Đáp án:** Hiển thị toàn bộ environment variables hiện có.  
- **Vì sao đúng:** `set` dump toàn bộ key=value, bao gồm PATH.  
- **Cách tự kiểm chứng:**  
```powershell
set | more
```
- **Lưu ý:** Kết quả có thể dài, nên pipe với `more`.

---

## Q4 (Bổ sung): Cách xem danh sách driver đã cài bằng CMD?
- **Đáp án:** `driverquery`.  
- **Vì sao đúng:** Đây là lệnh built-in để liệt kê driver, version, date.  
- **Cách tự kiểm chứng:**  
```powershell
driverquery | more
```
- **Lưu ý:** Output rất dài, nên pipe `| more` để xem theo trang.

---

## Q5 (Bổ sung): Lệnh `cls` có tác dụng gì?
- **Đáp án:** Xóa sạch màn hình CMD hiện tại.  
- **Vì sao đúng:** `cls` (clear screen) là tiện ích cơ bản của Windows CMD.  
- **Cách tự kiểm chứng:**  
```powershell
cls
```
- **Lưu ý:** Không xóa history, chỉ xóa phần hiển thị.

---

## Q6 (Bổ sung): Làm sao để xem help cho một lệnh?
- **Đáp án:** `help <command>` hoặc `<command> /?`.  
- **Vì sao đúng:** Đây là cách nhanh nhất để tra cứu syntax của lệnh trong CMD.  
- **Cách tự kiểm chứng:**  
```powershell
help systeminfo
systeminfo /?
```
- **Lưu ý:** Một số lệnh chỉ hỗ trợ cú pháp `/?.`

---

✅ Task 2 đã được giải thích theo format: **Đáp án → Vì sao đúng → Cách tự kiểm chứng → Lưu ý** (gồm 2 câu THM + 4 câu bổ sung).