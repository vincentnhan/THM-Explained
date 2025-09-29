# Windows Command Line – Task 4 (File and Disk Management) — Explained v1

---

## Q1 (THM): What are the file’s contents in C:\Treasure\Hunt?
- **Đáp án:** Dùng lệnh `type` để xem nội dung file (ví dụ `type C:\Treasure\Hunt\treasure.txt`).  
- **Vì sao đúng:** `type` hiển thị toàn bộ nội dung text file ngay trong CMD. Đây là yêu cầu chính của Task.  
- **Cách tự kiểm chứng:**
```powershell
type C:\Treasure\Hunt\treasure.txt
THM{CLI_POWER}
```
- **Lưu ý:** Nếu file dài, có thể dùng `more` để xem từng trang: `more C:\Treasure\Hunt\treasure.txt`.

---

## Q2 (Bổ sung): Cách xem thư mục hiện tại bằng CMD?
- **Đáp án:** `cd` hoặc `chdir`.  
- **Vì sao đúng:** Lệnh hiển thị đường dẫn working directory hiện tại.  
- **Cách tự kiểm chứng:**
```powershell
cd
chdir
```
- **Lưu ý:** Kết quả giống nhau, chỉ khác tên lệnh.

---

## Q3 (Bổ sung): Cách tạo và xóa thư mục?
- **Đáp án:** `mkdir <folder>` để tạo, `rmdir <folder>` để xóa.  
- **Vì sao đúng:** Đây là cặp lệnh chuẩn quản lý thư mục trong CMD.  
- **Cách tự kiểm chứng:**
```powershell
mkdir test_dir
dir
rmdir test_dir
```
- **Lưu ý:** Nếu thư mục có file, cần `rmdir /s /q <folder>` để xóa toàn bộ.

---

## Q4 (Bổ sung): Cách copy và move file?
- **Đáp án:** `copy <src> <dst>` và `move <src> <dst>`.  
- **Vì sao đúng:** `copy` tạo bản sao, `move` vừa copy vừa xóa file gốc.  
- **Cách tự kiểm chứng:**
```powershell
copy file1.txt file2.txt
move file2.txt C:\temp\
```
- **Lưu ý:** Có thể dùng wildcard `*` để copy nhiều file: `copy *.txt C:\backup`.

---

## Q5 (Bổ sung): Cách xóa file trong CMD?
- **Đáp án:** `del <file>` hoặc `erase <file>`.  
- **Vì sao đúng:** Hai lệnh tương đương, dùng để xóa file.  
- **Cách tự kiểm chứng:**
```powershell
del old.txt
erase old2.txt
```
- **Lưu ý:** Xóa bằng CMD không đưa vào Recycle Bin → cần cẩn trọng.

---

## Q6 (Bổ sung): Lệnh nào hiển thị cây thư mục?
- **Đáp án:** `tree`.  
- **Vì sao đúng:** `tree` hiển thị cấu trúc thư mục dưới dạng cây.  
- **Cách tự kiểm chứng:**
```powershell
tree C:\Users\strategos
```
- **Lưu ý:** Dùng `/f` để hiển thị cả file: `tree /f`.