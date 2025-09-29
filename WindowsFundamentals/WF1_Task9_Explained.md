# Windows Fundamentals 1 – Task 9 (Task Manager) — Explained v1

---

## Q1 (THM): What is the keyboard shortcut to open Task Manager?
- **Đáp án:** `Ctrl + Shift + Esc`.  
- **Vì sao đúng:** Đây là phím tắt trực tiếp mở Task Manager, nhanh hơn so với chuột phải Taskbar hoặc `Ctrl + Alt + Del`.  
- **Cách tự kiểm chứng:**  
```powershell
# Nhấn tổ hợp phím trên Windows
Ctrl + Shift + Esc
```
- **Lưu ý:** `Ctrl + Alt + Del` cũng mở màn hình tùy chọn có Task Manager, nhưng thêm 1 bước phụ.

---

## Q2 (Bổ sung): Task Manager có những tab chính nào?
- **Đáp án:** Processes, Performance, App history, Startup, Users, Details, Services.  
- **Vì sao đúng:** Đây là các tab mặc định trong Task Manager Windows 10/11.  
- **Cách tự kiểm chứng:**  
```powershell
# Mở Task Manager → More details → xem danh sách tab
```
- **Lưu ý:** Tùy phiên bản Windows, số tab có thể ít hơn (VD: Windows 7).

---

## Q3 (Bổ sung): Làm sao xem app nào chiếm CPU/RAM cao nhất?
- **Đáp án:** Trong tab *Processes*, sắp xếp cột CPU hoặc Memory.  
- **Vì sao đúng:** Task Manager hiển thị % CPU và MB RAM theo tiến trình.  
- **Cách tự kiểm chứng:**  
```powershell
# Mở Task Manager → Tab Processes → Click CPU hoặc Memory để sort
```
- **Lưu ý:** Các tiến trình nền (Background processes) cũng có thể tiêu tốn nhiều tài nguyên.

---

## Q4 (Bổ sung): Tab Startup có tác dụng gì?
- **Đáp án:** Quản lý ứng dụng khởi động cùng Windows.  
- **Vì sao đúng:** Startup ảnh hưởng tốc độ boot và hiệu suất hệ thống.  
- **Cách tự kiểm chứng:**  
```powershell
# Task Manager → Tab Startup → kiểm tra Status (Enabled/Disabled)
```
- **Lưu ý:** Chỉ disable app không cần thiết, tránh tắt driver/antivirus.

---

## Q5 (Bổ sung): Có thể dừng tiến trình trong Task Manager như thế nào?
- **Đáp án:** Chuột phải tiến trình → chọn *End task*.  
- **Vì sao đúng:** Đây là cách chuẩn để kết thúc process khi app bị treo.  
- **Cách tự kiểm chứng:**  
```powershell
# Task Manager → Tab Processes → chọn tiến trình → End task
```
- **Lưu ý:** Không nên end các tiến trình hệ thống (System, lsass.exe, winlogon.exe), có thể làm Windows crash.

---

✅ Task 9 đã được giải thích theo format: **Đáp án → Vì sao đúng → Cách tự kiểm chứng → Lưu ý** (gồm 1 câu THM + 4 câu bổ sung).