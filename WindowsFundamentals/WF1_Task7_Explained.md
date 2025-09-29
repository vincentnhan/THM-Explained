# Windows Fundamentals 1 – Task 7 (User Account Control) — Explained v1

---

## Q1 (THM): What does UAC mean?
- **Đáp án:** User Account Control.  
- **Vì sao đúng:** Đây là cơ chế bảo mật của Windows, nhằm hạn chế rủi ro khi chạy ứng dụng với quyền cao.  
- **Cách tự kiểm chứng:**  
	```powershell
  - Vào **Control Panel** → **User Accounts** → **Change User Account Control settings**.  
  - Chạy thử cài đặt phần mềm → thấy hộp thoại UAC yêu cầu xác nhận.  
  	```
- **Lưu ý:** UAC mặc định không áp dụng cho tài khoản built-in Administrator.

---

## Q2 (Bổ sung): Tại sao Microsoft giới thiệu UAC?
- **Đáp án:** Để giảm nguy cơ malware khai thác quyền admin mặc định.  
- **Vì sao đúng:** Trước Vista, user thường chạy quyền admin toàn thời gian, dễ bị tấn công.  
- **Cách tự kiểm chứng:** So sánh hành vi khi cài app trên Windows XP (không UAC) và Windows 10/11 (có UAC).  
- **Lưu ý:** Dù gây phiền, nhưng UAC là lớp phòng thủ quan trọng.

---

## Q3 (Bổ sung): Dấu hiệu nào cho biết ứng dụng yêu cầu UAC?
- **Đáp án:** Biểu tượng có hình chiếc khiên (shield icon).  
- **Vì sao đúng:** Windows tự động gắn icon này để báo hiệu hành động cần quyền cao.  
- **Cách tự kiểm chứng:** Quan sát icon installer `.exe` khi login bằng Standard User.  
- **Lưu ý:** Nếu thấy shield, cần chắc chắn nguồn file đáng tin cậy.

---

## Q4 (Bổ sung): Khi hiện prompt UAC thì các bước gì xảy ra?
- **Đáp án:** Windows yêu cầu xác nhận → hiển thị user admin mặc định → đợi nhập mật khẩu/OK.  
- **Vì sao đúng:** Đây là cơ chế *consent elevation* của Windows.  
- **Cách tự kiểm chứng:** Thử chạy app cài đặt khi đang dùng Standard User.  
- **Lưu ý:** Nếu không nhập mật khẩu sau thời gian chờ, UAC tự hủy và app không chạy.

---

## Q5 (Bổ sung): Có nên tắt UAC để khỏi phiền không?
- **Đáp án:** Không nên.  
- **Vì sao đúng:** Tắt UAC khiến malware dễ dàng chạy với quyền admin mà không bị ngăn chặn.  
- **Cách tự kiểm chứng:** Vào **User Account Control settings**, kéo xuống *Never notify* → thử cài app.  
- **Lưu ý:** Chỉ giảm mức cảnh báo nếu thực sự cần, tuyệt đối không nên tắt hẳn.

