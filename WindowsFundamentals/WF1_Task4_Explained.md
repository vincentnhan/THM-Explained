# Windows Fundamentals 1 – Task 4 (The File System) — Explained v1

---

## Q1 (THM): What is the meaning of NTFS?
- **Đáp án:** NTFS = New Technology File System.  
- **Vì sao đúng:** Đây là hệ thống tập tin mặc định của Windows hiện đại, thay thế FAT16/FAT32 và HPFS. NTFS hỗ trợ file > 4GB, phân quyền chi tiết, nén, mã hóa, và journaling để phục hồi sau sự cố.  
- **Cách tự kiểm chứng:** 
	```powershell
	Chuột phải ổ C: → Properties → sẽ thấy File System: NTFS.  
	 ``` 
- **Lưu ý:** FAT32 vẫn dùng cho USB/thẻ nhớ vì tương thích cao, nhưng hạn chế nhiều so với NTFS.  

---

## Q2 (Bổ sung): Điểm khác biệt chính giữa FAT32 và NTFS là gì?
- **Đáp án:** NTFS vượt trội vì hỗ trợ file lớn, phân quyền, nén, mã hóa, journaling. FAT32 thì không.  
- **Vì sao đúng:** FAT32 chỉ hỗ trợ file ≤ 4GB, không có tính năng bảo mật.  
- **Cách tự kiểm chứng:** Format USB bằng FAT32, thử copy file > 4GB → lỗi.  
- **Lưu ý:** Nếu cần di chuyển file lớn qua USB, nên chọn exFAT.  

---

## Q3 (Bổ sung): NTFS có tính năng nào giúp phục hồi khi hệ thống gặp sự cố?
- **Đáp án:** Journaling.  
- **Vì sao đúng:** NTFS ghi log các thay đổi, có thể tự động khôi phục folder/file khi crash. FAT32 không có.  
- **Cách tự kiểm chứng:** 
	```powershell
	Tắt đột ngột máy Windows, khi bật lại sẽ thấy quá trình **Checking file system (chkdsk)** dựa trên journaling.  
	```
- **Lưu ý:** Journaling giúp giảm mất mát dữ liệu nhưng không thay thế backup.  

---

## Q4 (Bổ sung): NTFS hỗ trợ những loại quyền nào trên thư mục/file?
- **Đáp án:** Full Control, Modify, Read & Execute, List folder contents, Read, Write.  
- **Vì sao đúng:** Đây là các quyền chuẩn được Microsoft quy định để kiểm soát truy cập.  
- **Cách tự kiểm chứng:** Chuột phải file/thư mục → Properties → tab Security → xem Group or user names.  
- **Lưu ý:** NTFS Permissions khác với Sharing Permissions; cần hiểu rõ khi cấu hình mạng.  

---

## Q5 (Bổ sung): Alternate Data Streams (ADS) dùng để làm gì?
- **Đáp án:** Cho phép lưu trữ nhiều stream dữ liệu trong 1 file (ngoài $DATA).  
- **Vì sao đúng:** ADS là tính năng NTFS, được dùng hợp pháp (đánh dấu file tải từ Internet) nhưng cũng có thể bị malware lợi dụng.  
- **Cách tự kiểm chứng:** Trong PowerShell:
  ```powershell
  notepad example.txt
  echo "hidden data" > example.txt:hidden
  Get-Item -Path .\example.txt -Stream *
  ```  
- **Lưu ý:** Khi điều tra forensics/DFIR, cần kiểm ADS để phát hiện dữ liệu ẩn.  

---

✅ Đây là phiên bản **Task 4 – Windows Fundamentals 1 (Explained)** theo format chuẩn giống Task 3: mỗi câu hỏi có **Đáp án → Vì sao đúng → Cách tự kiểm chứng → Lưu ý**.
