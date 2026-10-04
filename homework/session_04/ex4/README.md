# Báo cáo Bài 4: Quản lý .gitignore và Sửa lịch sử Commit (Amend)

## 1. Giải thích lệnh `git rm --cached`
- **Mục đích:** Gỡ bỏ một tệp tin ra khỏi chỉ mục (Index / Staging Area) của Git mà **không xóa file vật lý** trên đĩa cứng (Working Directory).
- **Cơ chế hoạt động:**
    - Lệnh thông thường `git rm <file>` sẽ xóa tệp cả ở vùng theo dõi lẫn ổ đĩa.
    - Tùy chọn `--cached` chỉ tác động lên Git Index, chuyển trạng thái tệp sang dạng "untracked" và chuẩn bị sẵn một thao tác xóa trong commit tiếp theo. Kết hợp đưa tệp vào `.gitignore`, Git sẽ hoàn toàn lờ tệp này đi trong các lần kiểm tra trạng thái tương lai.

## 2. Kết quả kiểm tra

### Trạng thái làm việc (`git status`)
```text
On branch main
nothing to commit, working tree clean