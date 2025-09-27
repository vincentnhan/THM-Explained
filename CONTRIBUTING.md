# Contributing Guide

## Giới thiệu (Vietnamese)
Cảm ơn bạn đã quan tâm đến repo này. Tài liệu ở đây được viết theo format **Explained Q&A** cho các module TryHackMe.  
Để giữ repo gọn gàng và dễ đọc, vui lòng làm theo các hướng dẫn dưới đây.

### Quy trình đóng góp
1. Fork hoặc clone repo:
   ```bash
   git clone https://github.com/vincentnhan/THM-Explained.git
   cd THM-Explained
   ```
2. Tạo branch mới (không commit trực tiếp vào `main`):
   ```bash
   git checkout -b feature/wf1-task2
   ```
3. Thêm hoặc chỉnh sửa file `.md` theo format:
   - Câu hỏi  
   - Đáp án  
   - Vì sao đúng  
   - Cách tự kiểm chứng  
   - Lưu ý  
4. Commit với message rõ ràng (theo convention):
   - `add:` thêm mới  
   - `fix:` sửa lỗi nội dung  
   - `docs:` thay đổi tài liệu  
   - Ví dụ:
     ```bash
     git commit -m "add: WF1 Task2 Explained"
     ```
5. Push lên branch của bạn:
   ```bash
   git push origin feature/wf1-task2
   ```
6. Tạo Pull Request vào `main`.

### Cập nhật CHANGELOG
- Nếu thay đổi lớn, thêm entry vào `CHANGELOG.md` dưới mục `[Unreleased]`.
- Khi release, đổi thành version + ngày.

---

## Introduction (English)
Thanks for contributing. This repo stores **TryHackMe Explained Q&A** notes.  
To keep things consistent, follow the steps below.

### Workflow
1. Fork or clone the repo:
   ```bash
   git clone https://github.com/vincentnhan/THM-Explained.git
   cd THM-Explained
   ```
2. Create a new branch (don’t commit directly to `main`):
   ```bash
   git checkout -b feature/wf1-task2
   ```
3. Add or edit `.md` files using the format:
   - Question  
   - Answer  
   - Why it is correct  
   - How to verify  
   - Notes  
4. Commit with clear messages (conventional style):
   - `add:` new content  
   - `fix:` correct content  
   - `docs:` update docs  
   - Example:
     ```bash
     git commit -m "add: WF1 Task2 Explained"
     ```
5. Push your branch:
   ```bash
   git push origin feature/wf1-task2
   ```
6. Open a Pull Request into `main`.

### Updating CHANGELOG
- For major updates, add an entry under `[Unreleased]` in `CHANGELOG.md`.
- When releasing, update with version + date.
