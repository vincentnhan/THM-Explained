# THM-Explained

## Giới thiệu (Vietnamese)
Repo này dùng để lưu lại các tài liệu học TryHackMe dưới dạng **Explained Q&A**.  
Mỗi task trong room sẽ được viết lại theo format:
- Câu hỏi  
- Đáp án  
- Vì sao đúng  
- Cách tự kiểm chứng  
- Lưu ý  

Mục tiêu là giúp việc học dễ hiểu hơn, và có thể đọc lại nhanh khi cần.

### Cấu trúc repo

```
THM-Explained/
├── WindowsFundamentals/    # Windows Fundamentals 1–3
├── ActiveDirectory/        # Active Directory Basics
├── CommandLine/            # Windows Command Line, Linux Shells...
├── Networking/             # OSI, TCP/IP, tools
├── Cryptography/           # Hashing, symmetric, asymmetric
├── ExploitationBasics/     # Exploit cơ bản
├── WebHacking/             # Web security labs
├── OffensiveSecurityTooling/
├── DefensiveSecurity/
├── SecuritySolutions/
├── DefensiveSecurityTooling/
└── Career/                 # Build your Cyber Security Career
```

### Cách đóng góp
1. **Clone repo** về máy:  
   ```
   git clone https://github.com/vincentnhan/THM-Explained.git
   cd THM-Explained
   ```
2. **Tạo branch mới** để làm việc (không commit trực tiếp vào `main`):  
   ```
   git checkout -b feature/wf1-task2
   ```
   > Đặt tên branch ngắn gọn, ví dụ: `feature/wf1-task2` hoặc `docs/update-readme`.
3. **Chỉnh sửa hoặc thêm file `.md`** theo đúng format Q&A Explained.  
   Ví dụ: `WindowsFundamentals/WF1_QA_v1.md`.
4. **Commit với message rõ ràng** (theo convention: `add:`, `fix:`, `docs:`...):  
   ```
   git add WindowsFundamentals/WF1_QA_v1.md
   git commit -m "add: WF1 Task2 Explained"
   ```
5. **Push lên GitHub**:  
   ```
   git push origin feature/wf1-task2
   ```
6. **Tạo Pull Request (PR)** từ branch vừa push vào `main`.  
   Trong PR mô tả ngắn gọn bạn đã thêm/sửa gì.

---

## Introduction (English)
This repo stores **TryHackMe Explained Q&A notes**.  
Each task is rewritten in a simple format:
- Question  
- Answer  
- Why it is correct  
- How to verify  
- Notes  

The goal is to make learning easier and to have quick references later.

### Repo structure
See the folder tree above for modules (WindowsFundamentals, AD, CommandLine, etc.).

### Contribution
1. **Clone the repo** to your local machine:  
   ```
   git clone https://github.com/vincentnhan/THM-Explained.git
   cd THM-Explained
   ```
2. **Create a new branch** (don’t commit directly to `main`):  
   ```
   git checkout -b feature/wf1-task2
   ```
3. **Edit or add `.md` files** following the Explained Q&A format.  
4. **Commit with a clear message** (e.g., `add: WF1 Task2 Explained`).  
5. **Push to GitHub**:  
   ```
   git push origin feature/wf1-task2
   ```
6. **Open a Pull Request (PR)** from your branch into `main`.  

---

## License
MIT License (optional, có thể thêm sau nếu cần).

## Changelog
Xem chi tiết thay đổi tại [CHANGELOG.md](CHANGELOG.md).
