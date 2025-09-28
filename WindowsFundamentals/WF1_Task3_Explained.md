# Windows Fundamentals 1 – Task 3 (Introduction to Windows) — Explained v1

---

## Q1 (THM): What is the required action in this task?
- **Đáp án:** Start the attached virtual machine (VM).  
- **Vì sao đúng:**  
  - Task này chỉ yêu cầu học viên khởi động máy ảo Windows được cung cấp.  
  - Đây là môi trường lab để thực hành các bước tiếp theo.  
- **Cách tự kiểm chứng:**  
  > Nhấn nút **Start Machine** trên TryHackMe.  
  > Chờ ~3 phút → VM sẵn sàng, có thể kết nối qua RDP (administrator / letmein123).  
- **Lưu ý:**  
  - Task 3 không có câu hỏi lý thuyết, chỉ là bước chuẩn bị môi trường.  
  - Đừng bỏ qua, vì các Task sau cần VM này để thao tác.  

---

## Q2 (Bổ sung): Tại sao TryHackMe yêu cầu sử dụng VM riêng thay vì Windows thật?
- **Đáp án:** Vì VM cô lập môi trường học tập, tránh rủi ro ảnh hưởng máy thật.  
- **Vì sao đúng:** Lab có thể yêu cầu quyền admin, thay đổi hệ thống, nên chạy trên VM là an toàn.  
- **Cách tự kiểm chứng:** Thử thay đổi settings trên VM (Control Panel, Taskbar) → không ảnh hưởng đến máy thật.  
- **Lưu ý:** Đây là nguyên tắc chung khi học security: thực hành trong môi trường cách ly.  

---

## Q3 (Bổ sung): Remote Desktop Protocol (RDP) dùng để làm gì?
- **Đáp án:** RDP cho phép kết nối từ xa tới máy Windows với giao diện đồ họa (GUI).  
- **Vì sao đúng:** Nó dùng port 3389, phổ biến trong môi trường doanh nghiệp.  
- **Cách tự kiểm chứng:** Trong VM/Windows thật, chạy:  
  ```cmd
  mstsc
  ```  
  → nhập IP của VM để kết nối.  
- **Lưu ý:** RDP thường là mục tiêu tấn công brute-force, nên cần bảo mật (MFA, firewall).  

---

## Q4 (Bổ sung): Khi Start Machine, tại sao cần chờ vài phút?
- **Đáp án:** Vì TryHackMe backend phải cấp phát tài nguyên, khởi động hệ điều hành, gắn IP công cộng.  
- **Vì sao đúng:** Đây là bản chất của cloud virtualization.  
- **Cách tự kiểm chứng:** Quan sát log hiển thị khi start machine (Loading, Assigning IP, Initializing).  
- **Lưu ý:** Nếu sau 5 phút chưa lên, nhấn **Stop Machine** rồi Start lại.  
