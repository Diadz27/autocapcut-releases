# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.7.1** - 2026-11-19 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.7.1.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.7.1.exe) (88,9 MB)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.7.1

- **Tái cấu trúc Studio Edit & Review (3 Sub-Studio chuyên biệt)**:
  - Tách bạch rõ ràng 3 không gian làm việc: `Review Phim Dài` (Ctrl+1), `AI Auto-Edit & Săn Highlight Viral` (Ctrl+2), và `Hậu Kỳ Độc Lập Cho Project` (Ctrl+3).
  - Tích hợp bộ 3 thẻ Visual Style 1-Click: Highlight Thể Thao Phonk Beat-Sync, Shorts Karaoke Cyan Dual-Track, và Sitcom Đa Vai.
- **Công nghệ 1-Click AI Auto-Edit Đa Tầng (Offline 100%, 0 Token AI)**:
  - Động cơ bắt nhịp Beat & Bass Drop bằng FFT chỉ 225ms.
  - Săn cao trào reo hò thể thao / bàn thắng kèm Dynamic Lookback Buffer (-10s -> +5s) trong 94ms.
  - Auto-Reframe 9:16 bám chuyển động với thuật toán RDP Decimation (<= 25 điểm/clip) giúp CapCut Desktop chạy mượt mà 60fps.
  - Phụ đề Karaoke Dual-Track đổi màu Cyan/Gold vi mô theo từng từ đang đọc.
- **Sửa triệt để lỗi giao diện & Khởi động sạch sẽ**:
  - Sửa lỗi tràn chữ, đè chữ tại bảng tùy chọn kịch bản: tái cấu trúc lưới .review-options-grid, chống va chạm giữa ô Bắt cảnh cao trào và Hook đầu video, hiển thị đầy đủ tên Model AI.
  - Khởi động sạch sẽ: Tự động dọn dẹp kịch bản cũ khi mở app và cất kín vào Recovery Storage để chỉ khôi phục khi người dùng chủ động chọn.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.7.1.exe -Algorithm SHA256
```

Kết quả phải là:

```
af1a85e7d6f37a7845a58274d141f2da777098f0f65e03755956b6c7cbb33255
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
