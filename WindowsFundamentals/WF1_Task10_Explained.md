# Windows Fundamentals 1 – Task 10 (Conclusion) — Explained v1

---

## Q1 (THM): [Không có câu hỏi chính thức trong Task 10]
- **Đáp án:** Không có (Task 10 chỉ là phần tổng kết).  
- **Vì sao đúng:**   
- **Cách tự kiểm chứng:** .  
- **Lưu ý:** Đây là phần kết thúc, chuẩn bị cho module kế tiếp.

---

## Q2 (Bổ sung): Sau Windows Fundamentals 1 thì nên học gì tiếp?
- **Đáp án:** Windows Fundamentals 2, 3 và Active Directory Basics.  
- **Vì sao đúng:** Đây là lộ trình được TryHackMe thiết kế, đi từ căn bản đến quản trị domain.  
- **Cách tự kiểm chứng:** 
```powershell
Vào module “Windows Fundamentals” trên TryHackMe, xem roadmap.  
```
- **Lưu ý:** Nên nắm chắc phần 1 trước khi học AD.

---

## Q3 (Bổ sung): Tại sao cần học Windows nội bộ khi làm Security?
- **Đáp án:** Vì phần lớn hạ tầng doanh nghiệp chạy Windows (server & endpoint).  
- **Vì sao đúng:** Security analyst/Red Team/Blue Team đều phải hiểu process, service, log Windows.  
- **Cách tự kiểm chứng:** 
```powershell
Xem lại các Task (Process, File System, User Account, UAC, Task Manager).  
```
- **Lưu ý:** Đây là kỹ năng nền tảng, áp dụng cả offensive & defensive.

---

## Q4 (Bổ sung): Các công cụ bảo mật mặc định của Windows là gì?
- **Đáp án:** Windows Defender, Windows Firewall, BitLocker, UAC, Event Viewer.  
- **Vì sao đúng:** Đây là công cụ built-in mà Microsoft cung cấp miễn phí.  
- **Cách tự kiểm chứng:**  
```powershell
Get-WindowsOptionalFeature -Online | findstr Windows
```
- **Lưu ý:** Một số tính năng chỉ có trên bản Pro/Enterprise (VD: BitLocker).

---

## Q5 (Bổ sung): Hướng đi nâng cao sau Fundamentals?
- **Đáp án:** Quản trị Windows Server, Active Directory, PowerShell, DFIR (Digital Forensics and Incident Response).  
- **Vì sao đúng:** Đây là kỹ năng cần cho SOC Analyst, Sysadmin, Pentester.  
- **Cách tự kiểm chứng:** 
```powershell
Theo dõi TryHackMe → Room Windows Fundamentals 2, 3, AD Basics.  
```
- **Lưu ý:** Có thể kết hợp lab ảo (VMware, VirtualBox, Proxmox) để luyện thực hành.

