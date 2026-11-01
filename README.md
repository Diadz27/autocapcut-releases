# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.4.3** - 2026-11-02 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.4.3.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.4.3.exe) (88,6 MB)
- [Tải gói ZIP kèm hướng dẫn cài đặt](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-v3.4.3.zip)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.4.3

- **Khắc phục triệt để lỗi link Douyin Modal & Tìm kiếm**:
  - Xử lý siêu tốc (<2 giây thay vì ~50 giây trước đây) cho link modal (`?modal_id=...`), link tìm kiếm (`/search/...`), và link dính emoji.
  - Tích hợp 3 CDN host dự phòng (api5, api3, api.amemv.com) với Android User-Agent chuẩn.
  - Loại bỏ hoàn toàn cảnh báo nhầm *"Không xác minh được ID video / video quảng cáo"*.
  - Tự động trích xuất chuẩn xác thời lượng và tiêu đề gốc.
- **Loại bỏ hoàn toàn tiến trình chạy ngầm (Zombie Process)**:
  - Tự động đóng và huỷ sạch cửa sổ ngầm `dyWin` và tất cả tiến trình con Whisper khi người dùng tắt cửa sổ chính của app.
  - Không còn tình trạng app chạy ngầm chiếm khóa trong Task Manager, đảm bảo mở lại ứng dụng luôn luôn thành công và mượt mà.
- **Hỗ trợ dán trực tiếp ID video Douyin (15-25 chữ số)** và tự động làm sạch emoji/kí tự đặc biệt.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.4.3.exe -Algorithm SHA256
```

Kết quả phải là:

```
b9f8ae09b4b8fb734ffe810283e354cede555240d99baa77f9baec19feed86ae
```

Mã SHA256 của gói ZIP (v3.4.3):

```
effdd3a2c1313313d1c76abc79ff4041a675f0c9906d9761ce9e99d0a848e17d
```

## Nếu Windows báo "Windows đã bảo vệ PC của bạn"?

Bấm **Thông tin khác → Chạy dù sao**.

Lý do: file cài đặt **chưa được ký chứng chỉ số** (Authenticode) nên Windows cảnh báo với mọi file mới của tác giả chưa ký. Đây không phải virus - hãy kiểm tra SHA256 ở trên nếu cần xác nhận.

## Bản trong release

| Tệp | Dùng để |
|---|---|
| `AutoCapCut-Setup-<phiên bản>.exe` | file cài đặt |
| `AutoCapCut-v3.4.3.zip` | gói ZIP kèm hướng dẫn cài đặt tiếng Việt |
| `latest.yml` | tệp feed cho cơ chế tự cập nhật (electron-updater) |
| `checksums.txt` | mã SHA256/SHA512 để kiểm tra file |
| `release-manifest.json` | thông tin bản + hash của `app.asar` và chữ ký Ed25519 |

## Dùng thử 2 giờ

Mở app, tại màn đăng nhập bấm **Dùng thử 2 giờ**. App tự tạo tài khoản dùng thử cho máy này và mở toàn bộ tính năng trong 2 giờ. Mỗi máy chỉ dùng thử 1 lần; hết 2 giờ app tự đăng xuất.

## Tự cập nhật

App tự kiểm tra bản mới mỗi lần mở (~10 giây), hoặc bấm thủ công **Cài đặt → Kiểm tra cập nhật**. Bản tải về được giữ lại trong `%APPDATA%\auto-capcut\updates-backup` để khôi phục.
