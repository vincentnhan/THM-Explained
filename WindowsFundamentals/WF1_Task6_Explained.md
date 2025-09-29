# Windows Fundamentals 1 – Task 6 (User Accounts, Profiles, and Permissions) — Explained v1

---

## Q1 (THM): What is the name of the other user account?
- **Đáp án:** (Tên hiển thị của user khác trong mục *Other users* / `lusrmgr.msc`).  
- **Vì sao đúng:** Windows lưu tất cả tài khoản cục bộ trong danh sách Users. Admin có thể xem và quản lý các account này.  
- **Cách tự kiểm chứng:**
	```powershell  
  - Mở **Run (Win+R)** → gõ `lusrmgr.msc`.  
  - Chọn **Users** → xem danh sách tài khoản.  
  ``` 
- **Lưu ý:** Trong môi trường Windows Home, `lusrmgr.msc` có thể không khả dụng.

---

## Q2 (THM): What groups is this user a member of?
- **Đáp án:** (Danh sách nhóm mà user thuộc, ví dụ *Users*, *Administrators*, …).  
- **Vì sao đúng:** Windows quản lý quyền dựa trên group membership. Khi gán user vào group, user sẽ thừa hưởng toàn bộ quyền của group đó.  
- **Cách tự kiểm chứng:** 
	```powershell  
	- `lusrmgr.msc` → Users → click double vào user → tab **Member Of**.  
	``` 
- **Lưu ý:** Một user có thể thuộc nhiều group cùng lúc.

---

## Q3 (THM): What built-in account is for guest access to the computer?
- **Đáp án:** `Guest`.  
- **Vì sao đúng:** Windows tạo sẵn tài khoản Guest cho phép đăng nhập hạn chế. Nó mặc định **disabled** vì rủi ro bảo mật.  
- **Cách tự kiểm chứng:**  
	```powershell 
	- `lusrmgr.msc` → Users → tìm account `Guest`.  
	``` 
- **Lưu ý:** Không nên bật Guest trong môi trường production.

---

## Q4 (THM): What is the account description?
- **Đáp án:** `Built-in account for guest access to the computer`.  
- **Vì sao đúng:** Đây là mô tả mặc định mà Microsoft gán cho tài khoản Guest.  
- **Cách tự kiểm chứng:**  
	```powershell 
	- `lusrmgr.msc` → Users → click `Guest` → xem **Description**.  
	``` 
- **Lưu ý:** Các bản Windows khác nhau có thể dịch mô tả sang ngôn ngữ hệ thống.

---

## Q5 (Bổ sung): Sự khác nhau giữa **Administrator** và **Standard User** là gì?
- **Đáp án:** Administrator có toàn quyền hệ thống; Standard User chỉ được thao tác trên file/thư mục của mình, không cài ứng dụng hệ thống.  
- **Vì sao đúng:** Quyền hạn quyết định khả năng chỉnh sửa setting, thêm/xóa user, cài đặt phần mềm.  
- **Cách tự kiểm chứng:**  
	```powershell 
	- Tạo Standard User → thử cài app → bị chặn hoặc yêu cầu quyền admin.
	```   
- **Lưu ý:** Nên dùng Standard User hàng ngày để giảm rủi ro bảo mật.

---

## Q6 (Bổ sung): Thư mục profile user nằm ở đâu?
- **Đáp án:** `C:\Users\<UserName>`.  
- **Vì sao đúng:** Khi user đăng nhập lần đầu, Windows tạo folder profile trong `C:\Users`.  
- **Cách tự kiểm chứng:**  
	```powershell 
	- Duyệt `C:\Users` → sẽ thấy folder tên giống account. 
	```   
- **Lưu ý:** Không xóa profile thủ công; dùng System Properties → Advanced → User Profiles.

---

## Q7 (Bổ sung): Công cụ nào quản lý Users & Groups?
- **Đáp án:** `lusrmgr.msc`.  
- **Vì sao đúng:** Đây là snap-in MMC cho quản lý Local Users và Groups.  
- **Cách tự kiểm chứng:**  
	```powershell 
	- Run → `lusrmgr.msc`.  
	``` 
- **Lưu ý:** Không có sẵn trên Windows Home Edition.

---

## Q8 (Bổ sung): Quyền được kế thừa từ Group hoạt động thế nào?
- **Đáp án:** Khi user tham gia Group, user thừa hưởng toàn bộ quyền gán cho Group đó.  
- **Vì sao đúng:** Windows áp dụng mô hình RBAC (Role-Based Access Control).  
- **Cách tự kiểm chứng:**  
	```powershell 
	- Thêm user vào group Administrators → user có thể cài ứng dụng, đổi setting hệ thống. 
	```   
- **Lưu ý:** Tránh gán user không cần thiết vào nhóm mạnh như Administrators.
