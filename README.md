# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.8.1** - 2026-11-28 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.8.1.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.8.1.exe) (88,9 MB)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.8.1

- **Review Phim luồng 3 bước & chọn thời lượng tổng**:
  - Sắp xếp rõ 3 bước (Chọn project & phụ đề → Chọn thời lượng & lời bình → Dựng CapCut), chọn mục tiêu ngay đầu luồng (`Theo lời bình`, `1 phút`, `3 phút`, `5 phút`, `10 phút`, hoặc tự nhập `phút:giây`), tự tính đoạn mở đầu vào quỹ thời lượng, dự báo trước khi ghi và tăng tốc phân tích media.
  - Sửa xoá sạch trạng thái DeepSeek cũ khi chuyển nguồn lời bình từ `DeepSeek` sang `Cục bộ`.
- **Phụ đề → Project CapCut trực tiếp**:
  - Trình xem & chỉnh sửa trực tiếp với 3 chế độ (`Giữ nguyên`, `Dễ đọc`, `Tuỳ chỉnh`), Sửa / Gộp / Tách câu giữ nguyên khoảng lặng và tạo nhanh project CapCut (tự giữ phụ đề khi gặp lỗi ghi hoặc đổi thiết lập).
  - Sửa đếm cộng dồn chính xác khi thử lại riêng câu lỗi và tự dọn trạng thái dịch cũ khi đổi chế độ định dạng hoặc gộp/tách câu.
- **Kết nối AI — Khôi phục DeepSeek (tuỳ chọn) & Storyboard AI (Gemini)**:
  - Gom `Gemini API Key` và `DeepSeek API Key` vào cùng mục `Kết nối AI` trong Cài đặt (mã hoá cục bộ bằng Windows DPAPI), dùng lại luồng DeepSeek viết lời bình Review Phim và dịch phụ đề trong Phụ đề / Reup / Douyin mà vẫn giữ thứ tự và mốc giờ.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.8.1.exe -Algorithm SHA256
```

Kết quả phải là:

```
87b4cf3a3c6e3d02ca1284b63c7ea809e4fd5b78ecdf08add39022f6b890da12
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
| `release-manifest.json` | thông tin bản phát hành và mã kiểm chứng toàn vẹn |

## Dùng thử 2 giờ

Mở app, tại màn đăng nhập bấm **Dùng thử 2 giờ**. App tự tạo tài khoản dùng thử cho máy này và mở toàn bộ tính năng trong 2 giờ. Mỗi máy chỉ dùng thử 1 lần; hết 2 giờ app tự đăng xuất.

## Tự cập nhật

App tự kiểm tra bản mới mỗi lần mở (~10 giây), hoặc bấm thủ công **Cài đặt → Kiểm tra cập nhật**. Bản tải về được giữ lại trong `%APPDATA%\auto-capcut\updates-backup` để khôi phục.
