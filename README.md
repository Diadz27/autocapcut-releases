# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.8.0** - 2026-11-26 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.8.0.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.8.0.exe) (88,7 MB)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.8.0

- **Storyboard AI (Kịch bản thành hình ảnh)**:
  - Dán kịch bản hoặc nạp `.srt` / `.txt` / `.vtt`, chia cảnh thông minh (hỗ trợ chia cảnh ngoại tuyến dự phòng giữ nguyên 100% nội dung), chỉnh sửa/tách/gộp/xoá cảnh, tạo prompt hình ảnh theo phong cách & góc máy, tạo ảnh bằng Gemini API và xuất Storyboard Pack đầy đủ.
  - Khoá Gemini API được mã hoá cục bộ bằng Windows DPAPI ngay trong Cài đặt, chỉ gọi API khi bạn bấm nút.
- **Review Phim offline gọn và dễ dùng hơn**:
  - 6 chip gợi ý luật chia phụ đề (bấm là điền, không cần nhớ cú pháp), badge hiển thị ngay thông số máy hiểu dưới ô lệnh, mẫu phong cách tự viết và nút Xoá luật.
- **Whisper cục bộ nâng cấp độ ổn định**:
  - Vá lỗi mất đoạn thoại cuối phim, chạy nền không đơ giao diện, tự bỏ cắt khoảng lặng (VAD) cho clip ngắn từ 60 giây trở xuống để giữ trọn đầu/cuối câu thoại và hiển thị tiến độ 4 pha rõ ràng.
- **Reup & Tải video đa nền tảng (Douyin / YouTube / Bilibili) gọn nhẹ**:
  - Hoạt động độc lập với Whisper cục bộ, phân vai ngoại tuyến và biến đổi Reup tránh bản quyền, khởi động nhanh và tập trung vào bộ công cụ dựng CapCut cốt lõi.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.8.0.exe -Algorithm SHA256
```

Kết quả phải là:

```
83bb33dba324d0fd1013b20962ca1f703ec1d8531c644d4d225db111f137ce49
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
