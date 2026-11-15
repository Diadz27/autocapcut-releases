# Auto CapCut - bản cài đặt chính thức

Repo này chỉ chứa **file cài đặt** (không chứa mã nguồn).

## Tải bản mới nhất

**v3.6.0** - 2026-11-15 · Windows 10/11 64-bit

- [Tải trực tiếp AutoCapCut-Setup-3.6.0.exe](https://github.com/Diadz27/autocapcut-releases/releases/latest/download/AutoCapCut-Setup-3.6.0.exe) (87,2 MB)
- [Trang Releases (tất cả phiên bản)](https://github.com/Diadz27/autocapcut-releases/releases)

> Đường dẫn `/releases/latest/download/...` **tự trỏ về bản mới nhất** khi có bản mới.

## Có gì mới ở 3.6.0

- **Không Gian Phân Tích Chuyên Sâu Đa Thể Loại (Deep Analysis Studio)**:
  - Tách riêng thành một mục độc lập trên thanh điều hướng chính, phục vụ đa dạng các nhu cầu sáng tạo ngoài phim ảnh (Bán hàng & Đánh giá sản phẩm/E-commerce USP, Công nghệ & Đánh giá cấu hình, Tin tức sự kiện xã hội, Bình phim chuyên sâu & Video Essay).
  - Bảo toàn 100% tính năng phân tích chuyên sâu truyền thống trong tab Review Phim (`reviewStyle = 'phan-tich'`).
- **Động Cơ Lọc Bỏ Phần Thừa Thông Minh (Smart Fluff Pruner)**:
  - Tự động phát hiện và loại bỏ các đoạn kêu gọi subscribe/like sáo rỗng, các từ đệm lan man, ngập ngừng (ừm, à, ờ, you know, actually) và khử lặp từ do nói vấp.
- **Trích Xuất Mốc Dẫn Chứng Thời Gian [mm:ss] (Timeline Proofs)**:
  - Gắn chính xác mốc thời gian minh chứng `[mm:ss]` vào từng luận điểm, so sánh, ưu/nhược điểm để biên tập viên nhảy thẳng đến cảnh quay tương ứng.
- **Bộ Nạp Kịch Bản Đa Năng & Tích Hợp CapCut Drafts**:
  - Hỗ trợ tải song song SubRip `.srt` hoặc văn bản `.txt` thô/có mốc thời gian.
  - Tự động sinh track kịch bản độc lập mang tên `AutoCapCut Phân Tích` trực tiếp vào project CapCut với 2 chế độ: gắn cờ dẫn chứng (`proof-markers`) và đọc nối tiếp (`sequential-narration`).
- **Tổng Rà Soát Chính Tả & Chuẩn Hóa Giao Diện Toàn Diện**:
  - Chuẩn hóa chính tả tiếng Việt có dấu trên toàn bộ 13 tab, modal cảnh báo, hộp thoại hệ thống native và từ điển đa ngôn ngữ i18n.

## Kiểm tra file đã tải (khuyến nghị 1 lần)

Mở PowerShell tại thư mục chứa file và chạy:

```powershell
Get-FileHash .\AutoCapCut-Setup-3.6.0.exe -Algorithm SHA256
```

Kết quả phải là:

```
315c1b89a53f360496310997e3f42b3cf0829542ef8f20fde4f1352a27458bec
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
