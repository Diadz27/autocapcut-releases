# Auto CapCut — bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.2.5** — 2026-10-21 · Windows 10/11 64-bit

- [⬇️ Tải trực tiếp AutoCapCut-Setup-3.2.5.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.2.5.exe) (88,5 MB)
- [⬇️ Tải gói ZIP kèm hướng dẫn cài đặt](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-v3.2.5.zip)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.2.5.exe -Algorithm SHA256
```

Kết quả phải là:

```
3a2ce96bfc477668ba478c2c68562c0449c5c92969322a22e8ac9738a6d896cf
```

Mã SHA256 của mỗi phiên bản nằm trong file `checksums.txt` đi kèm release.

Mã SHA256 của gói ZIP (v3.2.5):

```
2b6fa59877a180d05be65f16c02b1c1fdf45f6739e2edb18e734842d84b13d9c
```

## ⚠️ Windows báo "Windows đã bảo vệ PC của bạn"?

Bấm **Thông tin khác → Chạy dù đây**.

Lý do: file cài đặt **chưa được ký chứng chỉ số** (Authenticode) nên Windows cảnh báo với mọi file mới của tác giả chưa ký. Đây không phải virus — hãy kiểm tra SHA256 ở trên nếu cần xác nhận.

## Bản trong release

| Tệp | Dùng để |
|---|---|
| `AutoCapCut-Setup-<phiên bản>.exe` | file cài đặt |
| `AutoCapCut-v3.2.5.zip` | gói ZIP kèm hướng dẫn cài đặt tiếng Việt |
| `latest.yml` | tệp feed cho cơ chế tự cập nhật (electron-updater) |
| `checksums.txt` | mã SHA256/SHA512 để kiểm tra file |
| `release-manifest.json` | thông tin bản + hash của `app.asar` và chữ ký Ed25519 |

## Tự cập nhật

App tự kiểm tra bản mới mỗi lần mở (~10 giây), hoặc bấm thủ công **Cài đặt → Kiểm tra cập nhật**. Bản tải về được giữ lại trong `%APPDATA%\auto-capcut\updates-backup` để khôi phục.

## Lịch sử phiên bản

| Phiên bản | Ngày | Nội dung chính |
|---|---|---|
| **3.2.5** | 2026-10-21 | Sửa lỗi tải video Douyin "không có âm thanh" (loại luồng DASH, tự ghép hình + tiếng bằng FFmpeg khi Douyin phát 2 luồng riêng); đăng nhập theo đúng vai trò (trước đó mọi tài khoản đều là admin); mật khẩu lưu dạng băm bcrypt; app dùng khóa API công khai mới; chặn lệnh nội bộ khi chưa đăng nhập; kiểm tra SHA-256 cho FFmpeg/Whisper |
| 3.2.4 | 2026-10-21 | Sửa video Douyin 7–8 phút bị nhận nhầm thành 3 giờ; khôi phục tiếng Việt cho changelog 3.2.2; installer đổi tên theo phiên bản, bỏ tên "cracked" |
| 3.2.3 | 2026-10-21 | Bản vá trước đó |

Chi tiết từng mục nằm trong phần "Có gì mới" của app (tab **Cài đặt → Có gì mới**) và trong `release-notes.md` của từng release.

## Yêu cầu hệ thống

- Windows 10 / 11, 64-bit.
- Khoảng 600 MB trống (thêm ~1,7 GB nếu dùng mô hình Whisper cho phụ đề tự động).
- Mạng: dùng cho tự cập nhật, tải video Douyin và gọi AI (DeepSeek / Gemini).

## Gỡ cài đặt

Cài đặt Windows → Ứng dụng → Auto Cap Cut → Gỡ (hoặc chạy `Uninstall.exe` trong thư mục cài đặt). Dữ liệu người dùng nằm ở `%APPDATA%\auto-capcut` và không bị xoá khi gỡ.

## Hỗ trợ

Zalo / SĐT: _(thêm thông tin liên hệ tại đây)_

Khi báo lỗi, vui lòng gửi kèm ảnh chụp màn hình và phiên bản app (Cài đặt → Giới thiệu).
