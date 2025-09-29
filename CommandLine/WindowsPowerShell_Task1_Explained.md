# Windows PowerShell – Task 1 (Introduction) — Explained v2 (Fixed)

---

## Q1 (THM): [Không có câu hỏi chính thức trong Task 1]
- **Đáp án:** Không có (Task 1 chỉ giới thiệu, *No answer needed*).  
- **Vì sao đúng:** Nội dung gốc của room hiển thị phần giới thiệu, không đưa ra câu hỏi điền đáp án.  
- **Cách tự kiểm chứng:** 
```powershell
Kiểm tra lại Task 1 trong room *Windows PowerShell* — phần **Answer the questions below** hiển thị *No answer needed*.  
```
- **Lưu ý:** Các câu hỏi sẽ bắt đầu xuất hiện từ Task kế tiếp.

---

## Q2 (Bổ sung): PowerShell là gì (tóm tắt đúng trọng tâm)?
- **Đáp án:** Shell dòng lệnh + ngôn ngữ scripting quản lý **object**, có **cmdlet** dạng `Verb-Noun`.  
- **Vì sao đúng:** Điểm khác biệt cốt lõi với CMD: pipeline truyền **object** thay vì text.  
- **Cách tự kiểm chứng:**
```powershell
$PSVersionTable
Get-Process | Get-Member | Select-Object -First 5
```
- **Lưu ý:** Trên máy có thể tồn tại cả Windows PowerShell 5.x và PowerShell 7 (pwsh).

---

## Q3 (Bổ sung): Cách xem phiên bản PowerShell?
- **Đáp án:** `$PSVersionTable.PSVersion` hoặc `$PSVersionTable` để xem đầy đủ.  
- **Vì sao đúng:** Biến tự động chứa thông tin runtime hiện tại.  
- **Cách tự kiểm chứng:**
```powershell
$PSVersionTable.PSVersion
$PSVersionTable
```
- **Lưu ý:** Phiên bản ảnh hưởng hỗ trợ cmdlet/module.

---

## Q4 (Bổ sung): Tìm lệnh và trợ giúp như thế nào?
- **Đáp án:** `Get-Command` để tìm cmdlet; `Get-Help <cmdlet>` để xem tài liệu.  
- **Vì sao đúng:** Đây là 2 cmdlet căn bản để tự khám phá PowerShell.  
- **Cách tự kiểm chứng:**
```powershell
Get-Command *process*
Get-Help Get-Process -Online
```
- **Lưu ý:** Lần đầu có thể cần `Update-Help` (chạy với quyền admin).

---

## Q5 (Bổ sung): Pipeline hoạt động ra sao (demo nhanh)?
- **Đáp án:** Pipeline truyền **object** giữa cmdlet; có thể lọc/sắp xếp/chọn thuộc tính.  
- **Vì sao đúng:** Đây là “điểm ăn tiền” của PowerShell so với CMD.  
- **Cách tự kiểm chứng:**
```powershell
Get-Process | Where-Object CPU -gt 1 | Sort-Object CPU -Descending | Select-Object -First 5 Name,CPU,Id
```
- **Lưu ý:** Tránh pipe sang `Format-*` giữa pipeline tính toán vì sẽ “đóng” object thành chuỗi định dạng.

---

## Q6 (Bổ sung): Thực thi script bị chặn thì xử lý thế nào?
- **Đáp án:** Kiểm tra ExecutionPolicy và chọn mức phù hợp, ví dụ `RemoteSigned` cho user hiện tại.  
- **Vì sao đúng:** ExecutionPolicy là cơ chế an toàn ngăn chạy script không tin cậy.  
- **Cách tự kiểm chứng:**
```powershell
Get-ExecutionPolicy -List
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```
- **Lưu ý:** Không nên đặt `Unrestricted`/`Bypass` lâu dài; chỉ dùng tạm thời khi cần.