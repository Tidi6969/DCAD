# Biên bản đánh giá DFrame — V112

**Ngày ghi nhận:** 05/11/2026 (Asia/Bangkok)  
**Add-in:** DFrame  
**Repository module:** [Tidi6969/DFrame](https://github.com/Tidi6969/DFrame)  
**Danh mục hệ thống:** [Tidi6969/DCAD](https://github.com/Tidi6969/DCAD)  
**Chuẩn áp dụng:** [DCAD-STD-17 (Autoupdate)](https://github.com/Tidi6969/QuyUoc/blob/main/17_Autoupdate.md), mục 2.1, 8, 9.

> Biên bản này ghi nhận lời xác nhận theo ngữ cảnh yêu cầu của chủ dự án và chứng cứ GitHub. **Không phải bằng chứng AI đã build, NETLOAD hoặc chạy test trên CAD thực tế.**

## 1. Kết luận chung

- **Bản mới nhất trên nhánh main:** **V112**.
- **Phiên bản được ghi nhận nghiệm thu theo yêu cầu “Tương tự” DProject V17:** **V112**. Ở lượt liền trước, chủ dự án xác nhận DProject V17 “đã build chạy thử oke rồi”; sau đó yêu cầu “Tương tự https://github.com/Tidi6969/DFrame”. Việc ghi nhận build/chạy OK của V112 là cách hiểu theo ngữ cảnh đó, không phải một thông điệp kiểm thử độc lập nêu cụ thể từng CAD cho V112.
- **Baseline phát triển tiếp theo:** **V112**. Trước khi sửa cần đọc và xác minh ZIP/source V112.
- **Phiên bản tiếp theo nếu được yêu cầu phát triển mới:** V113 theo max+1; **lần này chưa tạo V113**.

## 2. Bằng chứng lưu trữ trên GitHub

| Hạng mục | Kết quả |
| --- | --- |
| ZIP trên main | [DFrame-V112.zip](https://github.com/Tidi6969/DFrame/blob/main/DFrame-V112.zip) |
| Đường dẫn ZIP thực tế | `DFrame-V112.zip` tại root |
| Kích thước | **7.467.098 byte** |
| Git blob SHA | `07c9dde40e7689711011e0cbce63069a1cdd559d` |
| Commit tải ZIP lên | [e4207cd4](https://github.com/Tidi6969/DFrame/commit/e4207cd44e07bd0bc247e619f465ca6ccaba3f9f) |
| V110 ZIP | Đã xóa khỏi `main` trước khi upload V112; nhật ký V110 vẫn có |
| V105/V99 ZIP | Đã xóa ở các lần trước, chỉ còn changelog trên main |
| CRC / SHA-256 / đọc source bên trong | `NotVerified` trong đợt chỉ cập nhật metadata |

## 3. Xác nhận từ chủ dự án

- Ngữ cảnh yêu cầu: **“Tương tự https://github.com/Tidi6969/DFrame”** ngay sau quy trình đồng bộ DProject V17 được người dùng xác nhận build và chạy thử OK.
- `UserReportedBuild=YES`, `UserReportedWorking=YES`, `UserReportedRuntime=YES` — ghi nhận theo ý nghĩa “tương tự” của yêu cầu trong ngữ cảnh.
- Không có danh sách CAD host hay log build/test V112 được cung cấp trong thông điệp này.
- **CAD target lịch sử:** AutoCAD 2022, AutoCAD 2025, GstarCAD 2027; không coi danh sách này là kết quả thử riêng V112.

## 4. Đánh giá theo bằng chứng

| Nội dung | Trạng thái | Ghi chú |
| --- | --- | --- |
| ZIP V112 hiện diện trên GitHub main | **PASS** | Đã đối chiếu Git blob và dung lượng |
| Ghi nhận chủ dự án yêu cầu nghiệm thu tương tự DProject | **UserConfirmedByContext** | Ghi nhận theo diễn đạt “Tương tự”, không phải log chạy thử |
| Build OK theo yêu cầu người dùng | **UserReported** | `UserReportedBuild=YES`, không xác minh log |
| Chạy/test OK theo yêu cầu người dùng | **UserReported** | `UserReportedWorking=YES`, không xác minh CAD host |
| Build PASS độc lập từng CAD host | **NotVerified** | Chưa có log V112 theo host |
| NETLOAD/Runtime PASS độc lập từng host | **NotVerified** | Chưa có test report V112 theo host |
| ZIP CRC/SHA-256/nội dung source | **NotVerified** | Không trích xuất ZIP trong lần này |
| Standards STD-01–18 | **NotVerified** | Chưa audit source/SDK V112 |
| README/changelog DFrame | **Đã cập nhật** | Ghi trạng thái V112, giữ lịch sử |
| Danh mục DCAD/README | **Đã cập nhật** | Ghi baseline V112 và link hồ sơ |
| Source và ZIP V112 | **Không thay đổi** | Không tạo V113 |

## 5. Tính liên tục và lưu trữ

V110 trước đây được xác nhận build/chạy/test OK và có [hồ sơ đánh giá](https://github.com/Tidi6969/DCAD/blob/main/Assessments/DFrame-V110.md). Trước lần đồng bộ này, ZIP V110 đã bị xóa khỏi nhánh chính, và ZIP V112 đã được upload. Changelog V99, V105 và V110 vẫn còn trên DFrame; không chỉnh sửa hoặc xóa các changelog lịch sử. Bản ZIP V112 hiện là ZIP duy nhất trên `main`; các commit Git cũ vẫn được giữ để tra cứu.

## 6. Liên kết và hướng xác minh tiếp

- [ZIP DFrame V112](https://github.com/Tidi6969/DFrame/blob/main/DFrame-V112.zip)
- [README DFrame](https://github.com/Tidi6969/DFrame/blob/main/README.md)
- [Changelog V112](https://github.com/Tidi6969/DFrame/blob/main/Change%20log/V112.txt)
- [Danh mục DCAD](https://github.com/Tidi6969/DCAD/blob/main/README.md)

Để ghi PASS kỹ thuật riêng từng CAD host, cần log build, host cụ thể, NETLOAD/smoke test và kết quả chạy chức năng. Để ghi PASS tiêu chuẩn và ZIP, phải đọc và kiểm tra nội dung gói. Việc đồng bộ này **không thay thế kiểm thử kỹ thuật độc lập**.
