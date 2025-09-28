# Windows Fundamentals 1 – Task 2 (The Desktop GUI) — Explained v1

---

## Q1 (THM): Which selection will hide/disable the Search box?
- **Đáp án:** Right-click Taskbar → Search → Hidden  
- **Vì sao đúng:**  
  - Windows 10/11 cho phép bật/tắt ô Search box trên Taskbar.  
  - Có ba tùy chọn: Hidden, Show search icon, Show search box.  
- **Cách tự kiểm chứng:**  
  1. Nhấp chuột phải Taskbar.  
  2. Vào **Search** → chọn **Hidden**.  
  3. Quan sát Search box biến mất.  
- **Lưu ý:**  
  - Trên Windows 11, mặc định là biểu tượng kính lúp (Search icon), không phải ô dài như Windows 10.  

---

## Q2 (THM): Which selection will hide/disable the Task View button?
- **Đáp án:** Right-click Taskbar → uncheck "Show Task View button"  
- **Vì sao đúng:**  
  - Nút Task View (hình 2 cửa sổ chồng nhau) cho phép xem các Virtual Desktops & timeline.  
  - Người dùng có thể tắt đi bằng menu chuột phải Taskbar.  
- **Cách tự kiểm chứng:**  
  1. Chuột phải Taskbar.  
  2. Bỏ chọn **Show Task View button**.  
  3. Nút Task View sẽ biến mất.  
- **Lưu ý:**  
  - Trên Windows 11, phím tắt **Win + Tab** vẫn mở Task View dù icon bị ẩn.  

---

## Q3 (THM): Besides Clock and Network, what other icon is visible in the Notification Area?
- **Đáp án:** Volume (Speaker icon)  
- **Vì sao đúng:**  
  - Notification Area (System Tray) luôn có **Clock**, **Network**, và **Volume** mặc định.  
- **Cách tự kiểm chứng:**  
  - Quan sát góc phải dưới Taskbar.  
  - Thấy biểu tượng loa (Volume) cạnh biểu tượng Wi-Fi/Network.  
- **Lưu ý:**  
  - Một số icon có thể ẩn trong mũi tên `^`, nhưng Clock/Network/Volume luôn hiện.  

---

## Q4 (Bổ sung): Desktop GUI và CLI khác nhau thế nào?
- **Đáp án:** GUI dùng thao tác trực quan (chuột, icon), CLI dùng command (text).  
- **Vì sao đúng:** GUI dễ cho người dùng phổ thông; CLI mạnh mẽ hơn với admin.  
- **Cách tự kiểm chứng:** So sánh thao tác mở File Explorer bằng **click icon** vs. **gõ `explorer.exe` trong CMD**.  
- **Lưu ý:** Trong bảo mật, CLI thường được ưa dùng để script hóa và audit.  

---

## Q5 (Bổ sung): Các thành phần chính của Taskbar gồm những gì?
- **Đáp án:** Start Menu, Search, Task View, Pinned Apps, Notification Area.  
- **Vì sao đúng:** Đây là layout mặc định từ Windows 10.  
- **Cách tự kiểm chứng:** Quan sát Taskbar và so với docs của Microsoft.  
- **Lưu ý:** Windows 11 thay đổi bố cục nhưng vẫn giữ nguyên các thành phần cơ bản.  

---

## Q6 (Bổ sung): Desktop icons mặc định lưu ở đâu trong filesystem?
- **Đáp án:** `C:\Users\<username>\Desktop`  
- **Vì sao đúng:** Đây là thư mục Desktop cá nhân của từng user profile.  
- **Cách tự kiểm chứng:** Mở File Explorer → gõ đường dẫn trên → sẽ thấy các icon hiện trên Desktop.  
- **Lưu ý:** Admin có thể cấu hình Group Policy để redirect Desktop folder sang server.  

---

## Q7 (Bổ sung): Notification Area có thể hiển thị thêm icon nào?
- **Đáp án:** Antivirus, Bluetooth, OneDrive, Battery (trên laptop).  
- **Vì sao đúng:** Notification Area là nơi ứng dụng chạy nền hiển thị trạng thái.  
- **Cách tự kiểm chứng:** Click mũi tên `^` để xem toàn bộ icon trong System Tray.  
- **Lưu ý:** Đây là nơi dễ bị malware lợi dụng để giả dạng icon hợp pháp.  
