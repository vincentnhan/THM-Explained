# Windows Fundamentals 1 — Task 1 (Windows Editions) — Explained v1

## Q1 (THM): What encryption can you enable on Pro that you can’t enable in Home?
- **Đáp án:** BitLocker  
- **Vì sao đúng:**  
  - BitLocker là tính năng mã hóa toàn bộ ổ đĩa, chỉ có trong bản **Windows Pro và Enterprise**.  
  - Phiên bản Home không hỗ trợ tính năng này (chỉ có một số máy có **Device Encryption** rút gọn).  
- **Cách tự kiểm chứng:**  
  > Mở `Control Panel → System and Security` → tìm **BitLocker Drive Encryption** (chỉ xuất hiện trên Pro/Enterprise).  
  > Hoặc CMD: `manage-bde -status` (máy Home sẽ báo không khả dụng).  
- **Lưu ý:**  
  - Các bản Pro thường có thêm: BitLocker, Group Policy, Domain Join, Remote Desktop Host, Hyper‑V.  
  - Khi làm lab bảo mật, nên dùng Pro/Enterprise để đầy đủ tính năng.

---

## Q2 (Bổ sung): Windows 10/11 Home và Pro khác nhau gì đáng chú ý?
- **Đáp án:** Pro có thêm các tính năng quản trị & bảo mật (BitLocker, Domain Join, Group Policy, Hyper‑V, Remote Desktop Host).  
- **Vì sao đúng:** Home hướng đến người dùng cá nhân; Pro hướng đến doanh nghiệp nên có nhiều công cụ kiểm soát.  
- **Cách tự kiểm chứng:** Tra bảng so sánh phiên bản trên Microsoft Docs.  
- **Lưu ý:** Nếu làm việc trong domain/AD, Home sẽ thiếu nhiều tính năng.

---

## Q3 (Bổ sung): Dòng thời gian các phiên bản Windows desktop nổi bật
- **Đáp án (tóm tắt):**  
  - **XP:** dễ dùng nhưng bảo mật yếu theo chuẩn hiện nay.  
  - **Vista:** giới thiệu **UAC**, hiệu năng gây tranh cãi.  
  - **7:** ổn định, rất phổ biến một thời.  
  - **8/8.1:** giao diện Metro, ít được ưa chuộng.  
  - **10:** cập nhật liên tục (Windows as a Service).  
  - **11:** UI mới, yêu cầu **TPM 2.0**, hỗ trợ phần cứng hiện đại.  
- **Vì sao đúng:** phản ánh các thay đổi lớn về bảo mật & trải nghiệm.  
- **Cách tự kiểm chứng:** Xem lịch sử phát hành trên trang Microsoft/Wikipedia.  
- **Lưu ý:** Một số bản đã **EOL** (hết hỗ trợ) — không nên dùng trong môi trường sản xuất.

---

## Q4 (Bổ sung): Windows Server khác Windows Client ở điểm nào?
- **Đáp án:** Windows Server tập trung cho hạ tầng doanh nghiệp: **Active Directory**, **DNS/DHCP**, **File/Print services**, **Hyper‑V**, role‑based features…  
- **Vì sao đúng:** thiết kế cho dịch vụ backend, ưu tiên tính ổn định, khả năng mở rộng & quản trị tập trung.  
- **Cách tự kiểm chứng:** Cài/lab Windows Server (2019/2022/2025) và mở **Server Manager** để xem **Roles & Features**.  
- **Lưu ý:** Chu kỳ hỗ trợ (LTSC) và chính sách cập nhật khác với Windows 10/11.
