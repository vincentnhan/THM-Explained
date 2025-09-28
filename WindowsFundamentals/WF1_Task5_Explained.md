# Windows Fundamentals 1 – Task 5 (The Windows\System32 Folders) — Explained v1

---

## Q1 (THM): What is the system variable for the Windows folder?
- **Đáp án:** `%windir%`  
- **Vì sao đúng:** Theo định nghĩa của Windows, *environment variables* lưu vị trí các thư mục hệ thống. Biến hệ thống cho thư mục Windows là **%windir%**, trỏ tới đường dẫn cài đặt Windows (thường là `C:\Windows`, nhưng có thể ở ổ/đường dẫn khác).  
- **Cách tự kiểm chứng:**  
  - **CMD:** `echo %windir%` → in ra đường dẫn.  
  - **PowerShell:** `$env:windir` → in ra đường dẫn.  
  - **Run (Win+R):** gõ `%windir%` → mở thư mục Windows.  
- **Lưu ý:** Không giả định Windows luôn nằm ở `C:\Windows`. Dùng `%windir%` trong script/lab để tương thích mọi máy.

---

## Q2 (Bổ sung): Vì sao thư mục **System32** quan trọng?
- **Đáp án:** `C:\Windows\System32` chứa các file hệ thống cốt lõi (DLL, EXE, driver, công cụ quản trị) mà Windows cần để hoạt động.  
- **Vì sao đúng:** Nhiều tiện ích chuẩn (ví dụ `cmd.exe`, `ipconfig.exe`, `tasklist.exe`, `reg.exe`, `sfc.exe`) và thư viện DLL hệ thống nằm tại đây; xóa/sửa sai có thể làm Windows không khởi động được.  
- **Cách tự kiểm chứng:**  
  - Mở **Run** → gõ `%windir%\System32` → xem danh sách công cụ.  
  - Chạy một số công cụ trong đó, ví dụ: `ipconfig`, `whoami`, `tasklist`.  
- **Lưu ý:** **Không** xóa/chỉnh sửa file trong System32 nếu không hiểu rõ. Dùng **SFC/DISM** để khôi phục nếu lỡ hỏng.

---

## Q3 (Bổ sung): Sự khác nhau giữa **System32** và **SysWOW64** trên Windows 64-bit là gì?
- **Đáp án:** Trên Windows 64-bit, **System32** chứa **binary 64-bit**, còn **SysWOW64** chứa **binary 32-bit** (WOW64 = Windows-on-Windows 64-bit, lớp tương thích chạy ứng dụng 32-bit).  
- **Vì sao đúng:** Kiến trúc Windows dùng cơ chế redirect để ứng dụng 32-bit truy cập thư mục/hive phù hợp; tên gọi gây nhầm nhưng là thiết kế tương thích ngược.  
- **Cách tự kiểm chứng:**  
  - Mở `%windir%\System32` và `%windir%\SysWOW64`, kiểm tra thuộc tính một số `.exe` bằng **Task Manager** → cột **Architecture** (hoặc dùng `dumpbin /headers` hay `Get-PEHeader` trong PowerShell module phù hợp).  
- **Lưu ý:** Khi copy/đăng ký DLL, hãy đảm bảo đúng “bitness” (32-bit vs 64-bit) để tránh lỗi `BadImageFormatException`.

---

## Q4 (Bổ sung): Cách xem và chỉnh **Environment Variables** an toàn?
- **Đáp án:** Vào **System Properties** → tab **Advanced** → **Environment Variables…**, hoặc dùng lệnh (`set`, `setx`, PowerShell `$env:`) để xem/chỉnh biến.  
- **Vì sao đúng:** Đây là cơ chế chuẩn của Windows để cấu hình đường dẫn hệ thống (như `%PATH%`, `%TEMP%`, `%windir%`) và biến người dùng.  
- **Cách tự kiểm chứng:**  
  - **CMD:** `set` (liệt kê), `echo %PATH%`.  
  - **PowerShell:** `gci Env:` hoặc `$env:PATH`.  
  - UI: `sysdm.cpl` → Advanced → Environment Variables.  
- **Lưu ý:** Khi thêm đường dẫn vào **PATH**, đặt sau System32 để ưu tiên công cụ hệ thống; tránh vượt quá độ dài PATH (nên gọn, dùng thư mục thay vì trỏ tới từng file).

---

## Q5 (Bổ sung): Làm sao gọi nhanh công cụ trong System32 mà không cần gõ đường dẫn đầy đủ?
- **Đáp án:** Nhờ biến **%PATH%** đã chứa `%windir%\System32`, nên có thể gọi trực tiếp (`ipconfig`, `ping`, `sfc`, …) từ CMD/PowerShell ở mọi thư mục.  
- **Vì sao đúng:** Windows tra cứu lệnh theo danh sách thư mục trong PATH; khi gặp tên khớp, nó thực thi binary tương ứng trong System32.  
- **Cách tự kiểm chứng:**  
  - Chạy `where ipconfig` hoặc `where cmd` → sẽ trả về đường dẫn trong `...\System32`.  
  - In PATH: `echo %PATH%` (CMD) hoặc `$env:Path` (PowerShell).  
- **Lưu ý:** Nếu thêm thư mục tùy chỉnh **đứng trước** System32 trong PATH và có file trùng tên, lệnh có thể bị "shadow"; cân nhắc thứ tự PATH để tránh rủi ro an ninh.

---

## Q6 (Bổ sung): Nếu System32 bị hỏng, nên kiểm tra/khôi phục thế nào?
- **Đáp án:** Dùng `sfc /scannow` và (nếu cần) `DISM /Online /Cleanup-Image /RestoreHealth`.  
- **Vì sao đúng:** **SFC** so sánh và khôi phục file hệ thống từ **Windows Resource Protection**; **DISM** có thể sửa ảnh hệ thống nếu nguồn SFC bị hỏng.  
- **Cách tự kiểm chứng:** Mở **CMD (Run as Administrator)** → chạy lần lượt các lệnh trên và kiểm tra log ở `%windir%\Logs\CBS\CBS.log`.  
- **Lưu ý:** Sao lưu dữ liệu trước khi can thiệp; tránh tắt máy giữa chừng.

---

✅ Task 5 đã được giải thích theo format chuẩn: **Đáp án → Vì sao đúng → Cách tự kiểm chứng → Lưu ý** cho câu hỏi THM và các câu hỏi bổ sung.
