# Biên bản đánh giá DBox — V15

**Ngày đánh giá:** 05/11/2026 (Asia/Bangkok)  
**Module:** DBox  
**Nguồn phiên bản:** [Tidi6969/DBox](https://github.com/Tidi6969/DBox)  
**Kho quản lý:** [Tidi6969/DCAD](https://github.com/Tidi6969/DCAD)  
**Quy chuẩn:** [Quy ước 17 — Autoupdate](https://github.com/Tidi6969/QuyUoc/blob/main/17_Autoupdate.md) §2.1, §8 và §9.

> Đây là biên bản ghi nhận xác nhận của chủ dự án và bằng chứng lưu trữ GitHub, **không phải biên bản build/test do trợ lý trực tiếp thực hiện**.

## 1. Kết luận

- **Bản mới nhất đã lưu trên main:** **DBox V15**.
- **Bản được chủ dự án xác nhận chạy OK:** **V15**.
- **Baseline mặc định:** V15; phải kiểm tra source/ZIP trước khi chỉnh sửa phần mềm.
- Nếu có yêu cầu phát triển bản tiếp theo mà không chỉ định phiên bản đích thì mặc định **V16**, nhưng **V16 chưa được tạo** trong lần ghi nhận này.

## 2. Đối chiếu thông tin GitHub

| Đặc tính | Giá trị |
| --- | --- |
| Đường dẫn ZIP | `DBox-V15.zip` tại root |
| [ZIP đã lưu](https://github.com/Tidi6969/DBox/blob/main/DBox-V15.zip) | Có, xác minh trên `main` |
| Dung lượng | 6.646.961 byte |
| Git blob SHA | `20b06f6544036527242a6a83c97f47b1c170489c` |
| Commit upload | [8a2a664](https://github.com/Tidi6969/DBox/commit/8a2a664dc3e9b5adacbbb5acb911a3ca4fbcca21), 05/11/2026 |
| Tình trạng V4 | ZIP/thư mục đã bị xóa khỏi `main`; còn nhật ký V4 và lịch sử Git |
| Bản gốc tạo ra V15 | Chưa xác minh |
| ZIP CRC / SHA-256 / kiểm tra source | `NotVerified` trong lượt đồng bộ |

## 3. Báo cáo chạy thử và đánh giá kỹ thuật

Chủ dự án xác nhận trong ChatGPT ngày 05/11/2026: **“Cái này anh cũng cập nhật như thế bản v15 đã chạy oke”.**

| Tiêu chí | Kết quả | Cơ sở |
| --- | --- | --- |
| ZIP V15 có trên GitHub | **PASS** | Xác nhận file, blob và kích thước |
| Người dùng xác nhận V15 chạy OK | **UserConfirmed** | `UserReportedWorking=YES` |
| Build V15 theo từng CAD host | **NotVerified** | Chưa có log build riêng và xác nhận build cụ thể |
| NETLOAD/runtime theo từng host | **NotVerified** | Chưa được nêu host và kịch bản thử |
| Kiểm tra toàn vẹn ZIP/CRC/SHA-256 | **NotVerified** | Chưa trích xuất/đọc lại gói binary |
| Tuân thủ quy ước source/SDK/thư mục | **NotVerified** | Chưa đánh giá nội dung ZIP V15 |
| Ghi nhận README/changelog trong DBox | **Đã cập nhật** | README và `Change log/V15.txt` |
| Đồng bộ danh mục DCAD | **Đã cập nhật** | DBox trong `DCAD/README.md` |

**CAD target theo lịch sử dự án:** AutoCAD 2022, AutoCAD 2025, GstarCAD 2027. Thông tin này không phải xác nhận V15 đã build/chạy trên cả ba host.

## 4. Hồ sơ các phiên bản

Trước đây V4 được chủ dự án xác nhận OK. Ngày 05/11/2026, V15 được upload vào nhánh `main` và thư mục ZIP V4 bị xóa qua commit [2bbe5f6](https://github.com/Tidi6969/DBox/commit/2bbe5f66d82ee72df4259c88a1f798d648ec50d2). Nhật ký V4 vẫn giữ; không khôi phục ZIP V4 hoặc xóa lịch sử Git. Bản nguồn của V15 và các thay đổi nghiệp vụ so với V4 chưa được chứng minh.

## 5. Kế hoạch xác minh kỹ thuật nếu cần

Để nâng `BuildStatus` hoặc `RuntimeStatus` thành PASS riêng theo CAD host, phải đối chiếu log biên dịch, DLL, lệnh NETLOAD và kết quả test từng host. Để đánh giá `StandardsStatus` và tính toàn vẹn ZIP, cần kiểm tra cấu trúc source/SDK và CRC/checksum. Không tự suy từ xác nhận chạy OK chung thành PASS cho từng CAD.

## 6. Dữ liệu liên kết

- [DBox-V15.zip](https://github.com/Tidi6969/DBox/blob/main/DBox-V15.zip)
- [DBox README](https://github.com/Tidi6969/DBox/blob/main/README.md)
- [Changelog V15](https://github.com/Tidi6969/DBox/blob/main/Change%20log/V15.txt)
- [DCAD README](https://github.com/Tidi6969/DCAD/blob/main/README.md)

**Phạm vi thực hiện:** chỉ cập nhật dữ liệu quản lý và đánh giá trên GitHub, không chỉnh sửa code, ZIP, hoặc tạo phiên bản phần mềm mới.
