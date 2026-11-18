# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.7.0** - 2026-11-18 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.7.0.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.7.0.exe) (87,4 MB)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.6.5

- **Nâng cấp độ ổn định tính năng "Phân tích AI" — Săn Highlight & Tự động Cắt Clip Ngắn Viral**:
  - Xử lý an toàn video có kích thước khung hình lẻ khi giữ khung gốc hoặc đốt phụ đề, tự động kiểm tra và chặn các mốc cắt vượt quá độ dài video gốc, đồng thời phục hồi trọn vẹn danh sách clip ngay cả khi phản hồi AI bị ngắt giữa chừng.
  - Giữ đồng bộ hình–tiếng chính xác tuyệt đối khi cắt clip trực tiếp trên timeline Project CapCut có khoảng trống giữa các đoạn video và tự dọn âm thanh dư ngoài vùng cắt.
  - Đồng bộ chỉnh sửa mốc thời gian `[mm:ss]` trực tiếp lên file phụ đề `.srt` xuất ra và chống bấm đúp khi đang cắt trên CapCut.
- **Kế thừa trọn vẹn tính năng v3.7.0**:
  - Săn Highlight & Tự động Cắt Clip Ngắn Viral (TikTok / Shorts / Reels) chấm điểm 0–100, Hook 3s + Caption + Hashtag, cắt hàng loạt MP4 (Giữ gốc / Cắt nhanh Copy / 9:16 Crop / 9:16 Nền mờ / 1:1 / Đốt phụ đề) kèm `.srt` + `_post.txt` và tải video đa nền tảng YouTube / Bilibili / Douyin ổn định.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.7.0.exe -Algorithm SHA256
```

Kết quả phải là:

```
28dd8e1c6b72be1f852363607d6dc947d8b7d05ef50039a184a30caa072d3f87
```

Mã SHA256 của mỗi phiên bản nằm trong file `checksums.txt` đi kèm release.

## Nếu Windows báo "Windows đã bảo vệ PC của bạn"?

Bấm **Thông tin khác → Chạy dù sao**.

Lý do: file cài đặt **chưa được ký chứng chỉ số** (Authenticode) nên Windows cảnh báo với mọi file mới của tác giả chưa ký. Đây không phải virus - hãy kiểm tra SHA256 ở trên nếu cần xác nhận.

## Dùng thử 2 giờ

Mở app, tại màn đăng nhập bấm **Dùng thử 2 giờ**. App tự tạo tài khoản dùng thử cho máy này và mở toàn bộ tính năng trong 2 giờ. Mỗi máy chỉ dùng thử 1 lần; hết 2 giờ app tự đăng xuất.

## Tự cập nhật

App tự kiểm tra bản mới mỗi lần mở (~10 giây), hoặc bấm thủ công **Cài đặt → Kiểm tra cập nhật**. Bản tải về được giữ lại trong `%APPDATA%\auto-capcut\updates-backup` để khôi phục.
