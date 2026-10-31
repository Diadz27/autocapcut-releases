# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.4.2** - 2026-11-01 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.4.2.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.4.2.exe) (88,7 MB)
- [Tải gói ZIP kèm hướng dẫn cài đặt](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-v3.4.2.zip)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.4.2

- **Hệ thống phân vai đa phương thức SOTA (Multimodal Speaker Diarization)**:
  - Tự động nhận diện và gán tên nhân vật nói theo ngữ cảnh, phân tích âm thanh cao độ F0 (Nam/Nữ) và thị giác (Gemini Vision AI / Offline Heuristic cho video/phim dài đến 120 phút).
  - Tích hợp bảng nhân vật (Character Roster) thông minh trên các tab Dịch phụ đề và Reup.
- **Khắc phục triệt để video Douyin Ads**: Lọc bỏ 100% video quảng cáo, thương mại và tài trợ trong quá trình trích xuất/tải Douyin.
- **Tối ưu tốc độ AI & Bộ nhớ đệm**: Tắt chế độ suy nghĩ (Thinking Mode) không cần thiết ở các tác vụ dịch phụ đề để phản hồi nhanh hơn 10-30s; bổ sung LRU Cache lưu tạm các câu dịch trùng lặp (0ms, $0).
- **Quốc tế hoá tiếng Gruzia (Georgian - ka)**: Bổ sung gói giao diện tiếng Gruzia và hỗ trợ dịch/review.
- **Bảo toàn 100% tính năng Tạo ảnh (WS32)**: Tạo ảnh tuỳ chọn từ prompt (Gemini API & Google Flow) kèm mã hoá cookie DPAPI.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.4.2.exe -Algorithm SHA256
```

Kết quả phải là:

```
66f934be9285e08ee18eb6a0c47ad91bbbb68245a9aac8f2b572ca57f170bb97
```

Mã SHA256 của mỗi phiên bản nằm trong file `checksums.txt` đi kèm release.

Mã SHA256 của gói ZIP (v3.4.2):

```
9e487051e7ebad01fb5feb27411ada68622b9b7f30014211a5d4108a452d7fdc
```

## Nếu Windows báo "Windows đã bảo vệ PC của bạn"?

Bấm **Thông tin khác → Chạy dù sao**.

Lý do: file cài đặt **chưa được ký chứng chỉ số** (Authenticode) nên Windows cảnh báo với mọi file mới của tác giả chưa ký. Đây không phải virus - hãy kiểm tra SHA256 ở trên nếu cần xác nhận.

## Bản trong release

| Tệp | Dùng để |
|---|---|
| `AutoCapCut-Setup-<phiên bản>.exe` | file cài đặt |
| `AutoCapCut-v3.4.2.zip` | gói ZIP kèm hướng dẫn cài đặt tiếng Việt |
| `latest.yml` | tệp feed cho cơ chế tự cập nhật (electron-updater) |
| `checksums.txt` | mã SHA256/SHA512 để kiểm tra file |
| `release-manifest.json` | thông tin bản + hash của `app.asar` và chữ ký Ed25519 |

## Dùng thử 2 giờ

Mở app, tại màn đăng nhập bấm **Dùng thử 2 giờ**. App tự tạo tài khoản dùng thử cho máy này và mở toàn bộ tính năng trong 2 giờ. Mỗi máy chỉ dùng thử 1 lần; hết 2 giờ app tự đăng xuất.

## Tự cập nhật

App tự kiểm tra bản mới mỗi lần mở (~10 giây), hoặc bấm thủ công **Cài đặt → Kiểm tra cập nhật**. Bản tải về được giữ lại trong `%APPDATA%\auto-capcut\updates-backup` để khôi phục.
