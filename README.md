# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.7.3** - 2026-11-19 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.7.3.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.7.3.exe) (89,0 MB)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.7.3

- **Khắc phục triệt để lỗi Whisper DLL 3221225781 (0xC0000135) & Auto CPU Fallback**:
  - Tự động tiêm đường dẫn `PATH` chứa DLL và thiết lập thư mục làm việc chuẩn xác trước khi gọi runtime Whisper GPU.
  - Cơ chế tự tải kèm bản CPU 3.5MB dự phòng khi tải mô hình GPU, tự động chuyển đổi mượt mà sang CPU khi GPU crash hoặc thiếu phụ thuộc driver, đảm bảo nhận dạng giọng nói không bao giờ gián đoạn.
  - Bộ lọc chống lặp từ và đồng bộ bù trừ thời gian VAD giúp phụ đề khớp khẩu hình chính xác.
- **Tích hợp Công nghệ AI Voiceover & Audio Ducking Đa Tầng**:
  - Tự động hạ âm lượng nền (audio ducking) video gốc xuống 15% (-16.5dB) ngay khi xuất hiện giọng thuyết minh AI.
  - Giữ âm lượng Hook 3 giây đầu ở mức 25% tạo độ hút người xem, tự động lùi mốc phát giọng đọc AI sau phân đoạn Hook để tránh xung đột âm thanh.
- **Bảo Mật Cấp Cao Ed25519 & Cổng Gói Khách Hàng Fail-Closed**:
  - Chữ ký bất đối xứng Ed25519 bảo vệ `app.asar`, loại bỏ hoàn toàn HMAC secret, thực thi chính sách fail-closed tuyệt đối.
  - Gói ZIP thương mại tuân thủ whitelist 2 tệp duy nhất, đối soát SHA-256 trùng khớp 100%, ngăn chặn hoàn toàn rò rỉ mã nguồn.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.7.3.exe -Algorithm SHA256
```

Kết quả phải là:

```
a1ecd2bf85a889316cef51656ade1f14da2d634da94ea3e312289140e3c69fac
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
