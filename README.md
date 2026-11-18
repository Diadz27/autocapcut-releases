# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.6.3** - 2026-11-18 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.6.3.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.6.3.exe) (87,4 MB)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.6.3

- **Nâng cấp đột phá mục "Phân tích AI" — Săn Highlight & Tự động Cắt Clip Ngắn Viral (TikTok / Shorts / Reels)**:
  - Tách biệt rõ ràng với Review Phim: AI tự săn các khoảnh khắc đắt giá nhất, chấm điểm Viral (0–100), tạo Hook 3 giây đầu + Caption + Hashtag sẵn đăng và cho phép tinh chỉnh trực tiếp mốc cắt `[mm:ss - mm:ss]`.
  - Tự động cắt hàng loạt video ngắn ra file MP4 (hỗ trợ Giữ khung gốc, Cắt nhanh Copy gốc, Dọc 9:16 Crop tâm, Dọc 9:16 Nền mờ điện ảnh, Vuông 1:1 và đốt phụ đề) kèm sẵn file phụ đề `.srt` và gói đăng bài `_post.txt`.
  - Hỗ trợ cắt trực tiếp các đoạn clip highlight ngay trên timeline Project CapCut chỉ với 1 bấm chuột.
- **Tải video đa nền tảng ổn định hơn**:
  - Khắc phục lỗi tải YouTube (HTTP 403 & header lớn), hỗ trợ link Bilibili `/vi/video/BV...` & vượt HTTP 412, nhận diện link Douyin dạng `/share/note/` và chặn triệt để video quảng cáo.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.6.3.exe -Algorithm SHA256
```

Kết quả phải là:

```
f34728ca8c4ccccdcc1b410f0a07e428fba87a6b6b3b181a2738c8ff9162bb5d
```

Mã SHA256 của mỗi phiên bản nằm trong file `checksums.txt` đi kèm release.

## Nếu Windows báo "Windows đã bảo vệ PC của bạn"?

Bấm **Thông tin khác → Chạy dù sao**.

Lý do: file cài đặt **chưa được ký chứng chỉ số** (Authenticode) nên Windows cảnh báo với mọi file mới của tác giả chưa ký. Đây không phải virus - hãy kiểm tra SHA256 ở trên nếu cần xác nhận.

## Dùng thử 2 giờ

Mở app, tại màn đăng nhập bấm **Dùng thử 2 giờ**. App tự tạo tài khoản dùng thử cho máy này và mở toàn bộ tính năng trong 2 giờ. Mỗi máy chỉ dùng thử 1 lần; hết 2 giờ app tự đăng xuất.

## Tự cập nhật

App tự kiểm tra bản mới mỗi lần mở (~10 giây), hoặc bấm thủ công **Cài đặt → Kiểm tra cập nhật**. Bản tải về được giữ lại trong `%APPDATA%\auto-capcut\updates-backup` để khôi phục.
