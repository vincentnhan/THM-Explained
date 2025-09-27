# Windows Command Line — Task 1 (Introduction) — Explained v1

## Q1. (THM) What is the default command line interpreter in the Windows environment?
- **Đáp án:** `cmd.exe`  
- **Vì sao đúng:** Đây là trình thông dịch dòng lệnh mặc định của hệ điều hành Windows, thường được gọi là **Command Prompt**.  
- **Cách tự kiểm chứng:**  
  > Nhấn `Win + R` → gõ `cmd` → Enter.  
  > Cửa sổ Command Prompt xuất hiện, trong Task Manager sẽ thấy process **cmd.exe**.  
- **Lưu ý:** Windows có thêm PowerShell và Windows Terminal, nhưng mặc định lâu đời vẫn là `cmd.exe`.  

---

## Q2. (Bổ sung) Vì sao CLI (Command-Line Interface) có thể hiệu quả hơn GUI (Graphical User Interface)?
- **Đáp án:** CLI nhanh, ít tốn tài nguyên, dễ tự động hóa, thuận tiện cho quản lý từ xa.  
- **Vì sao đúng:**  
  - GUI trực quan nhưng nhiều thao tác chuột, trong khi CLI chỉ cần gõ lệnh.  
  - CLI không tốn nhiều tài nguyên đồ họa, phù hợp cho hệ thống cũ hoặc máy chủ.  
  - Có thể viết script/batch để lặp lại thao tác.  
  - Quản lý từ xa qua SSH hiệu quả ngay cả khi mạng yếu.  
- **Cách tự kiểm chứng:**  
  > So sánh: kiểm tra IP bằng GUI (`Control Panel → Network`) mất nhiều thao tác; trong khi gõ `ipconfig` trong cmd là xong.  
- **Lưu ý:** CLI ban đầu khó học nhưng về lâu dài tiết kiệm thời gian cho quản trị viên.  

---

## Q3. (Bổ sung) Các mục tiêu học tập (Learning Objectives) của room này là gì?
- **Đáp án:**  
  1. Hiển thị thông tin hệ thống cơ bản.  
  2. Kiểm tra và xử lý sự cố mạng.  
  3. Quản lý file và thư mục.  
  4. Kiểm tra các tiến trình đang chạy.  
- **Vì sao đúng:** Đây là danh sách được nêu rõ trong phần *Learning Objectives* của room.  
- **Cách tự kiểm chứng:**  
  > Đọc phần giới thiệu của task trên TryHackMe.  
- **Lưu ý:** Những kỹ năng này là nền tảng để tiếp cận các task sau (Basic Info, Network, File/Process).  

---

## Q4. (Bổ sung) Trước khi bắt đầu room này, cần prerequisite gì?
- **Đáp án:** Hoàn thành module **Windows and AD Fundamentals**.  
- **Vì sao đúng:** Room yêu cầu kiến thức cơ bản về Windows và Active Directory.  
- **Cách tự kiểm chứng:**  
  > Xem phần *Room Prerequisites* trong tài liệu.  
- **Lưu ý:** Nếu chưa nắm AD và Windows Fundamentals, người học có thể khó hiểu các ví dụ trong đây.  

---

## Q5. (Bổ sung) Làm sao để kết nối vào máy lab trong room này?
- **Đáp án:** Sử dụng **AttackBox** hoặc SSH với thông tin:  
  - Username: `user`  
  - Password: `Tryhackme123!`  
- **Vì sao đúng:** TryHackMe cung cấp máy ảo cho bài thực hành. Có thể dùng AttackBox tích hợp sẵn hoặc SSH từ AttackBox vào target VM.  
- **Cách tự kiểm chứng:**  
  > Nhấn **Start AttackBox** → mở terminal → chạy lệnh: `ssh user@MACHINE_IP`  
  > Nhập password `Tryhackme123!` (sẽ không hiển thị ký tự).  
- **Lưu ý:** Đây chỉ là lab credential, không dùng cho môi trường thực tế.  

