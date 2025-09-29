# Windows Fundamentals 1 – Task 8 (Settings and the Control Panel) — Explained v1

---

## Q1 (THM): In the Control Panel, change the view to Small icons. What is the last setting in the Control Panel view?
- **Đáp án:** (Tên mục cuối cùng trong danh sách Small icons – tùy phiên bản Windows, thường là *Windows Defender Firewall* hoặc *Windows Tools*).  
- **Vì sao đúng:** Khi chuyển sang Small icons, Control Panel hiển thị toàn bộ mục theo alphabet, mục cuối tùy phiên bản.  
- **Cách tự kiểm chứng:**  
```powershell
control.exe /name Microsoft.ControlPanel
→ View by → Small icons → kéo xuống cuối danh sách.  
```
- **Lưu ý:** Trên Windows 10/11 có thể khác nhau chút, nhưng đều theo thứ tự alphabet.

---

## Q2 (Bổ sung): Sự khác nhau cơ bản giữa Settings và Control Panel?
- **Đáp án:** Settings dành cho cấu hình hiện đại (UI đơn giản, touch-friendly), Control Panel cho cấu hình nâng cao & legacy.  
- **Vì sao đúng:** Microsoft chuyển dần chức năng sang Settings, nhưng nhiều tính năng nâng cao vẫn chỉ có ở Control Panel.  
- **Cách tự kiểm chứng:** 
```powershell
Start → tìm *Network & Internet* → *Change adapter options* → tự động mở Control Panel.  
```
- **Lưu ý:** Không nên nghĩ Settings đã thay thế hoàn toàn Control Panel.

---

## Q3 (Bổ sung): Cách mở nhanh Control Panel bằng lệnh?
- **Đáp án:** `control` hoặc `control.exe`.  
- **Vì sao đúng:** Đây là binary gốc của Windows cho Control Panel.  
- **Cách tự kiểm chứng:**  
```powershell
Win + R → control
```
- **Lưu ý:** Có thể thêm tham số, ví dụ `control printers` để mở trực tiếp Printers.

---

## Q4 (Bổ sung): Tìm setting nào nên dùng Search trong Start?
- **Đáp án:** Nếu không chắc mục nằm ở Settings hay Control Panel.  
- **Vì sao đúng:** Start menu Search sẽ trả kết quả đúng, ví dụ gõ *wallpaper* → dẫn tới Settings.  
- **Cách tự kiểm chứng:**  
```powershell
# Không cần PowerShell, chỉ cần Start → gõ từ khóa như wallpaper, firewall
```
- **Lưu ý:** Đây là cách nhanh nhất cho end-user.

---

## Q5 (Bổ sung): Tại sao Microsoft vẫn giữ Control Panel song song Settings?
- **Đáp án:** Vì nhiều app/setting cũ chưa được migrate sang Settings.  
- **Vì sao đúng:** Control Panel hỗ trợ backward compatibility, tránh gây lỗi cho ứng dụng cũ.  
- **Cách tự kiểm chứng:** 
```powershell
So sánh Settings vs Control Panel, ví dụ *Device Manager* chỉ mở qua Control Panel.  
```
- **Lưu ý:** Tương lai Control Panel có thể bị thay thế hoàn toàn, nhưng chưa phải bây giờ.

