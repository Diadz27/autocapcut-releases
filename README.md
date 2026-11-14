# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.5.0** - 2026-11-14 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.5.0.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.5.0.exe) (88,7 MB)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.5.0

- **Khắc phục triệt để xưng hô loạn xạ (Natural Kinship Localization)**:
  - Tự động nhận diện ngữ cảnh và chuẩn hóa quan hệ xưng hô tiếng Việt (bố - mẹ - con, vợ - chồng, anh - em, sếp - nhân viên).
  - Loại bỏ hoàn toàn tình trạng dịch máy vô cảm gọi bố mẹ là "bạn", vợ chồng gọi nhau là "tôi - bạn".
- **Ngụy trang & Lách từ nhạy cảm TikTok / Reels (Social Word Camouflage)**:
  - 3 cấp độ ngụy trang (Tắt / Nhẹ nhàng / Mạnh mẽ) tự động chuyển đổi các từ cấm/nhạy cảm (chết, máu, bạo lực, tình dục, lừa đảo, cờ bạc...) sang từ lóng reup tự nhiên tiếng Việt (bay màu, đăng xuất, si rô, xôi thịt...).
  - Áp dụng thuật toán Regex Unicode boundary chuẩn xác 100% cho tiếng Việt có dấu.
- **Khung Prompt AI tùy chỉnh & Chip chèn biến trong Reup Content**:
  - Giao diện trực quan cho phép người dùng tùy biến chỉ thị dịch thuật, phong cách văn phong riêng và chèn nhanh các biến ngữ cảnh qua chip bấm 1-click.
- **6 Cấu hình AI Thông minh 1-Click (Smart Translation Profiles)**:
  - Tích hợp sẵn 6 preset tối ưu: Siêu phẩm TikTok/Reels, Phim gia đình/Drama, Cổ trang/Tiên hiệp, Tổng tài/Đô thị, Tài liệu/Khoa học, Chuyên gia (Tùy chỉnh).
- **Hỗ trợ toàn diện đa nền tảng Windows & macOS (Plan B)**:
  - Đồng bộ hoá đường dẫn thư viện CapCut, hiệu ứng và bản dựng draft chuẩn xác trên cả 2 hệ điều hành.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.5.0.exe -Algorithm SHA256
```

Kết quả phải là:

```
70652e98a424676521e3efb8ec167f6bcf5c8a300bf61ff24fe6fdc9105998e8
```

Mã SHA256 của mỗi phiên bản nằm trong file `checksums.txt` đi kèm release.

## Nếu Windows báo "Windows đã bảo vệ PC của bạn"?

Bấm **Thông tin khác → Chạy dù sao**.

Lý do: file cài đặt **chưa được ký chứng chỉ số** (Authenticode) nên Windows cảnh báo với mọi file mới của tác giả chưa ký. Đây không phải virus - hãy kiểm tra SHA256 ở trên nếu cần xác nhận.

## Bản trong release

| Tệp | Dùng để |
|---|---|
| `AutoCapCut-Setup-<phiên bản>.exe` | file cài đặt |
| `latest.yml` | tệp feed cho cơ chế tự cập nhật (electron-updater) |
| `checksums.txt` | mã SHA256/SHA512 để kiểm tra file |
| `release-manifest.json` | thông tin bản + hash của `app.asar` và chữ ký Ed25519 |

## Dùng thử 2 giờ

Mở app, tại màn đăng nhập bấm **Dùng thử 2 giờ**. App tự tạo tài khoản dùng thử cho máy này và mở toàn bộ tính năng trong 2 giờ. Mỗi máy chỉ dùng thử 1 lần; hết 2 giờ app tự đăng xuất.

## Tự cập nhật

App tự kiểm tra bản mới mỗi lần mở (~10 giây), hoặc bấm thủ công **Cài đặt → Kiểm tra cập nhật**. Bản tải về được giữ lại trong `%APPDATA%\auto-capcut\updates-backup` để khôi phục.