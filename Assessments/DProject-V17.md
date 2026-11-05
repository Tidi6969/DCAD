# Biên bản đánh giá DProject — V17

**Ngày đối chiếu:** 05/11/2026 (Asia/Bangkok)  
**Module:** DProject  
**Repository module:** [Tidi6969/DProject](https://github.com/Tidi6969/DProject)  
**Kho quản lý:** [Tidi6969/DCAD](https://github.com/Tidi6969/DCAD)  
**Quy chuẩn:** [Quy ước 17 — Autoupdate](https://github.com/Tidi6969/QuyUoc/blob/main/17_Autoupdate.md), mục 2.1, 8, 9.

> Đây là báo cáo lưu xác nhận của chủ dự án cùng bằng chứng tồn tại trên GitHub, không phải biên bản kiểm thử kỹ thuật độc lập.

## 1. Tóm tắt đánh giá

- **Bản mới nhất có ZIP trên nhánh main:** **V17**.
- **Bản đã được chủ dự án xác nhận build và chạy thử OK:** **V17**.
- **Baseline mặc định cho lần phát triển tiếp theo:** V17, cần kiểm tra source/ZIP trước khi sửa.
- **Phiên bản đích mặc định cho yêu cầu thay đổi code tiếp theo:** V18, theo STD-17 max+1. **Không tạo V18 khi chỉ cập nhật metadata**.
- **Nguồn kỹ thuật tạo V17:** chưa được xác minh (không suy ra là V16/V13).

## 2. Đối chiếu GitHub

| Hạng mục | Kết quả |
| --- | --- |
| Tệp ZIP | [DProject-V17.zip](https://github.com/Tidi6969/DProject/blob/main/DProject-V17.zip) |
| Đường dẫn trong repo | `DProject-V17.zip` (thư mục gốc) |
| Kích thước | **6.668.493 byte** |
| Git blob SHA | `8f72bc7b9401bb7018dbb0dd8455b6ad60761e7f` |
| Commit upload ZIP | [23d6f290](https://github.com/Tidi6969/DProject/commit/23d6f290651674c3106342c6730d5b44b4e2d001), 05/11/2026 |
| ZIP V12, V13 | Đã bị xóa khỏi nhánh `main` trước lần cập nhật này; changelog và Git history còn |
| Kiểm chứng bên trong ZIP / CRC / SHA-256 | `NotVerified` trong lần đồng bộ |

## 3. Phản hồi của chủ dự án

Trong ChatGPT ngày 05/11/2026, chủ dự án xác nhận: **“Cập nhật lại thông tin bản V17 này đã build chạy thử oke rồi.”**

- `UserReportedBuild=YES`: Chủ dự án báo build thành công.
- `UserReportedWorking=YES` và `UserReportedRuntime=YES`: Chủ dự án báo đã chạy thử OK.
- Không có danh sách CAD host được kiểm thử riêng trong thông điệp này. **Không tự gán PASS cho mỗi CAD host** nếu chưa có chứng cứ riêng.
- CAD target lịch sử theo hồ sơ V13: AutoCAD 2022, AutoCAD 2025, GstarCAD 2027. Danh sách lịch sử không chứng minh V17 đã được thử đủ cả ba host.

## 4. Bảng đánh giá

| Tiêu chí | Trạng thái | Cơ sở |
| --- | --- | --- |
| Tồn tại ZIP V17 trên GitHub main | **PASS** | Git tree trả về đúng blob và kích thước |
| Build thành công theo người dùng | **UserConfirmed** | `UserReportedBuild=YES` |
| Chạy thử thành công theo người dùng | **UserConfirmed** | `UserReportedWorking=YES`, `UserReportedRuntime=YES` |
| Build PASS độc lập từng CAD host | **NotVerified** | Chưa đối chiếu log theo host |
| NETLOAD/Runtime PASS độc lập từng host | **NotVerified** | Chưa có hồ sơ test theo host |
| ZIP CRC/SHA-256/kiểm tra cấu trúc | **NotVerified** | Chưa đọc nội dung ZIP trong lần này |
| Source/References/Standards STD-01–18 | **NotVerified** | Chưa rà soát code ZIP V17 |
| README/changelog DProject | **Đã cập nhật** | README và `Change log/V17.txt` |
| Danh mục DCAD | **Đã cập nhật** | Ghi V17 là phiên bản mới nhất và đã được người dùng xác nhận |
| Thay đổi ZIP/code | **Không** | Chỉ cập nhật metadata |

## 5. Lịch sử

Changelog V12 và V13 vẫn được giữ lại ở repository DProject. ZIP/thư mục V12 và V13 đã bị chủ repository xóa khỏi cây main ngày 05/11/2026, các commit lịch sử không bị xóa. V17 ZIP là ZIP phiên bản duy nhất được ghi nhận trên main tại thời điểm đối chiếu.

## 6. Nguồn và liên kết

- [DProject V17 ZIP](https://github.com/Tidi6969/DProject/blob/main/DProject-V17.zip)
- [README DProject](https://github.com/Tidi6969/DProject/blob/main/README.md)
- [Changelog V17](https://github.com/Tidi6969/DProject/blob/main/Change%20log/V17.txt)
- [Danh mục DCAD](https://github.com/Tidi6969/DCAD/blob/main/README.md)

**Kết luận:** V17 là bản mới nhất được chủ dự án xác nhận build và chạy thử OK. Ghi nhận trung thực theo báo cáo; kiểm chứng kỹ thuật độc lập theo từng host chưa có bằng chứng để tuyên bố PASS.
