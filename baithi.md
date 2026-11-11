# BÀI LÀM – HACKATHON 02

- **Mã đề:** 08
- **Họ tên:Nguyễn Trọng Nhân 7
- **Lớp:CNTT2
- **Link repository:**
- **Hệ điều hành (Windows/macOS):Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy
 pwq
 ls -force
 cp quy_trinh_thu_am.txt .\docs\
 mkdir backup
 cp .\data\lich_thu_thang_8.xlsx .\backup\
 rm *.tmp
 cd .\logs\
 get-childitem -recurse -force
# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng
PS D:\starter-kit\starter-kit\Phong_Thu_Am_Website> ls -force


    Directory: D:\starter-kit\starter-kit\Phong_Thu_Am_Website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026   1:45 PM                data
d-----        11/11/2026   1:42 PM                docs
d-----        11/11/2026   1:43 PM                evidence
d-----        11/11/2026   1:45 PM                logs
d-----        11/11/2026   1:34 PM                web
-a----         11/3/2026   7:08 AM             74 .env
-a----         11/3/2026   7:08 AM           2409 bai_lam.md
-a----         11/3/2026   7:08 AM            157 Quy_Trinh_Thu_Am.txt
-a----         11/3/2026   7:08 AM             22 temp_808.tmp

    Directory: D:\starter-kit\starter-kit\Phong_Thu_Am_Website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026   1:52 PM                backup
PS D:\starter-kit\starter-kit\Phong_Thu_Am_Website\logs> ls -force


    Directory: D:\starter-kit\starter-kit\Phong_Thu_Am_Website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:08 AM            992 Studio.log

    Directory: D:\starter-kit\starter-kit\Phong_Thu_Am_Website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026   1:54 PM                backup
d-----        11/11/2026   1:45 PM                data
d-----        11/11/2026   1:51 PM                docs
d-----        11/11/2026   1:43 PM                evidence
d-----        11/11/2026   1:45 PM                logs
d-----        11/11/2026   1:34 PM                web
-a----         11/3/2026   7:08 AM             74 .env
-a----         11/3/2026   7:08 AM           2409 bai_lam.md
-a----         11/3/2026   7:08 AM            157 Quy_Trinh_Thu_Am.txt


    Directory: D:\starter-kit\starter-kit\Phong_Thu_Am_Website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:08 AM           6136 lich_thu_thang_8.xlsx


    Directory: D:\starter-kit\starter-kit\Phong_Thu_Am_Website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:08 AM           6136 Lich_Thu_Thang_8.xlsx


    Directory: D:\starter-kit\starter-kit\Phong_Thu_Am_Website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:08 AM            157 quy_trinh_thu_am.txt


    Directory: D:\starter-kit\starter-kit\Phong_Thu_Am_Website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:08 AM            992 Studio.log


    Directory: D:\starter-kit\starter-kit\Phong_Thu_Am_Website\web


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026   1:34 PM                images
-a----         11/3/2026   7:08 AM            586 app.js
-a----         11/3/2026   7:08 AM            514 index.html
-a----         11/3/2026   7:08 AM            460 style.css


    Directory: D:\starter-kit\starter-kit\Phong_Thu_Am_Website\web\images


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:08 AM           3097 logo-soundlab.png


### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
(Dán kết quả vào đây – xoá dòng này)

```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

 
# Ghi lệnh vào đây (xoá dòng này)

 select-string "status=500" .\logs\studio.log >.\logs\loi_500.txt

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
(Dán kết quả vào đây – xoá dòng này)

```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell
# Ghi lệnh vào đây (xoá dòng này)

 (get-content .\logs\studio.log | select-string "status=404").count

```text
(Dán kết quả đếm vào đây – xoá dòng này)
4
## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
# Ghi lệnh vào đây (xoá dòng này)
#script: tong_hop.ps1
#tac gia: NGUYEN_TRONG_NHAN
#Ngay tao: 11-11-2026
Write-Host "Dang tao bao cao..."
"=== BAO CAO SU CO WEBSITE ===" > Phong_Thu_Am_Website
Get-Content .\logs\studio.log | select-string "status=404"
Get-Content .\logs\studio.log | select-string "status=404" | Measure-Object
Write-Host "Hoan thanh!"

```text
(Dán nội dung file vào đây – xoá dòng này)

```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 |  |  |  |
| 2 |  |  |  |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** 
- **Expected:** 
- **Actual:** 
- **Log:** 

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/lich_thu_thang_8.xlsx`, không cần ghi vào đây.
