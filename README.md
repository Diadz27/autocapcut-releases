# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.4.6** - 2026-11-08 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.4.6.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.4.6.exe) (88,7 MB)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.4.6

- **Đồng bộ thị giác Review Phim (Visual Action Grounding First)**:
  - Bắt buộc 100% câu kể bắt đầu bằng hành động vật lý cụ thể trên màn hình (quay mặt, mở cửa, rút súng, vấp ngã...), áp dụng cho toàn bộ phong cách kịch bản (`kich-tinh`, `phan-tich`, `hai-huoc`, `tau-hai`, `truc-quan`).
  - Khóa dải phụ đề cực hẹp (1–4 dòng phụ đề, 3–15s phim) ngăn chặn triệt để hiện tượng AI sinh câu bình ngoài lề không liên quan tới hình ảnh.
- **Triệt tiêu trôi dạt tích luỹ (Zero Cumulative Drift)**:
  - Cài đặt cơ chế Scene-Bounded Anchor: Triệt tiêu hoàn toàn hiện tượng video chạy vượt xa phụ đề sau nhiều câu thoại.
  - Tự do chuyển góc máy (Reverse Shot) tại cảnh đầu của câu mới mà không bị phạt điểm.
  - Ưu tiên giữ trọn 1 cú máy liền mạch tự nhiên (1–2 cuts) cho câu ngắn, tránh băm nhỏ video thành nhiều nhát giật cục.
- **Bảo toàn cao độ âm thanh CapCut**: Luôn sinh speed material với chuẩn `{ tone: true }` trong CapCut Draft Schema v1.5.0 bảo toàn cao độ giọng đọc.
- **Hoàn thiện hạ tầng cập nhật tự động (Auto-Update Checksum Integrity)**:
  - Đồng bộ 100% mã băm SHA-512 base64 và file size vào `latest.yml`, loại bỏ hoàn toàn lỗi `sha512 checksum mismatch` khi người dùng tự động cập nhật trong app.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.4.6.exe -Algorithm SHA256
```

Kết quả phải là:

```
50761f737fc7f9c6caf702f77fd11fa2a72afc1eedd055e7ae85af2b9aff9edf
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
