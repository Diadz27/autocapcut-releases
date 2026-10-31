# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.4.0** - 2026-10-30 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.4.0.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.4.0.exe) (88,5 MB)
- [Tải gói ZIP kèm hướng dẫn cài đặt](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-v3.4.0.zip)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.4.0

- Tab **Tạo Prompt** có thêm bước **tạo ảnh tuỳ chọn** (mặc định TẮT): bật lên mới thấy phần cấu hình, ai chỉ cần prompt chữ thì tab giống hệt 3.3.0.
- 2 engine: **Gemini API** (cần key Gemini đã bật thanh toán) hoặc **Google Flow** (cần Chrome + cookie labs.google + gói Google AI Pro/Ultra — dùng hạn mức gói, không thu thêm tiền).
- Chọn chất lượng theo mục đích, khung 16:9 / 9:16 / 1:1 / 4:5 / 3:4; xem trước số ảnh + chi phí ước tính (USD + VND) rồi mới bấm chạy; trên 50 ảnh phải xác nhận.
- Ảnh lưu `001_...` đúng thứ tự prompt, có nút **Mang sang Đồng bộ thông minh**, thử lại từng ảnh lỗi, huỷ vẫn giữ ảnh đã xong.
- Cookie Google Flow nay được mã hoá bằng Windows DPAPI (trước đây lưu văn bản thường).

> Chi phí tạo ảnh là **tham khảo** theo bảng giá Google và có thể thay đổi. Lần đầu nên bấm "Tạo thử 3 ảnh" hoặc "Tự kiểm tra engine (1 ảnh)" để chắc key/gói dùng được.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.4.0.exe -Algorithm SHA256
```

Kết quả phải là:

```
ad1533667d79ad6247b5db0f90da9a2d3578b1407396cbbf2bd475c139a6c25f
```

Mã SHA256 của mỗi phiên bản nằm trong file `checksums.txt` đi kèm release.

Mã SHA256 của gói ZIP (v3.4.0):

```
0f0f382b6e8733972da18c83bf244ddda418991c57caefbbcd9fc09549ce0e37
```

## Nếu Windows báo "Windows đã bảo vệ PC của bạn"?

Bấm **Thông tin khác → Chạy dù sao**.

Lý do: file cài đặt **chưa được ký chứng chỉ số** (Authenticode) nên Windows cảnh báo với mọi file mới của tác giả chưa ký. Đây không phải virus - hãy kiểm tra SHA256 ở trên nếu cần xác nhận.

## Bản trong release

| Tệp | Dùng để |
|---|---|
| `AutoCapCut-Setup-<phiên bản>.exe` | file cài đặt |
| `AutoCapCut-v3.4.0.zip` | gói ZIP kèm hướng dẫn cài đặt tiếng Việt |
| `latest.yml` | tệp feed cho cơ chế tự cập nhật (electron-updater) |
| `checksums.txt` | mã SHA256/SHA512 để kiểm tra file |
| `release-manifest.json` | thông tin bản + hash của `app.asar` và chữ ký Ed25519 |

## Dùng thử 2 giờ

Mở app, tại màn đăng nhập bấm **Dùng thử 2 giờ**. App tự tạo tài khoản dùng thử cho máy này và mở toàn bộ tính năng trong 2 giờ. Mỗi máy chỉ dùng thử 1 lần; hết 2 giờ app tự đăng xuất.

## Tự cập nhật

App tự kiểm tra bản mới mỗi lần mở (~10 giây), hoặc bấm thủ công **Cài đặt → Kiểm tra cập nhật**. Bản tải về được giữ lại trong `%APPDATA%\auto-capcut\updates-backup` để khôi phục.
