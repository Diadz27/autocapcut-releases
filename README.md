# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.6.1** - 2026-11-18 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.6.1.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.6.1.exe) (87,3 MB)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.6.1

- **Mở rộng khối "Tải video" đa nền tảng (Douyin / YouTube / Bilibili)**:
  - Hỗ trợ trích xuất và tải đồng bộ luồng media công khai (không DRM) cho **YouTube** và **Bilibili** bên cạnh **Douyin** theo cùng luồng xử lý và tuỳ chọn sẵn có.
  - Hiển thị thông báo tiếng Việt rõ ràng khi gặp video riêng tư, có DRM, trả phí/VIP, livestream, yêu cầu đăng nhập, giới hạn vùng hoặc anti-bot.
- **Chuẩn hoá phân giải link & Chống tải nhầm video quảng cáo**:
  - Hỗ trợ tách và chuẩn hoá URL từ văn bản chia sẻ (kể cả đường dẫn CJK + tham số `modal_id`/`p`), xử lý chuyển hướng link rút gọn (`youtu.be`, `youtube.com/shorts`, `b23.tv`, `v.douyin.com`) và loại bỏ tham số tracking/playlist.
  - Lọc triệt để video quảng cáo (pre-roll, overlay, banner, `uuu_265.mp4`, `adPlacements`, `raw_ad_data`) và cô lập luồng theo đúng ID mục tiêu.
- **Đổi tên giao diện & Sửa lỗi cắt chữ Sidebar**:
  - Đồng bộ đổi tên hiển thị mục/tab/giao diện khối tải video thành **"Tải video"** trên mọi bản dịch i18n (`vi` / `en` / `es` / `ka`).
  - Rút gọn nhãn nút sidebar **"Phân tích chuyên sâu"** thành **"Phân tích AI"** kèm chỉnh CSS chống tràn/cắt chữ trên mọi kích thước cửa sổ.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.6.1.exe -Algorithm SHA256
```

Kết quả phải là:

```
7fd94e777bd892ec10a14b61086d2a3d7ba2007df016c6309118adad138d1e7a
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
