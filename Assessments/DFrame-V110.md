# Biên bản đánh giá DFrame — V110

**Ngày đối chiếu:** 05/11/2026 (Asia/Bangkok)  
**Add-in:** DFrame  
**Repository module:** [Tidi6969/DFrame](https://github.com/Tidi6969/DFrame)  
**Repository danh mục:** [Tidi6969/DCAD](https://github.com/Tidi6969/DCAD)  
**Quy ước:** [DCAD-STD-17](https://github.com/Tidi6969/QuyUoc/blob/main/17_Autoupdate.md), đặc biệt §2.1, §8, §9  
**Loại hồ sơ:** đánh giá trạng thái bản đã được chủ dự án xác nhận, **không phải kết quả kiểm thử độc lập do AI thực hiện**

## 1. Kết quả chung

- **Phiên bản mới nhất thực sự đang lưu:** **V110**.
- **Phiên bản được chủ dự án xác nhận đã build và chạy/test OK:** **V110**.
- **Bản chuẩn (baseline) mặc định cho lần phát triển kế tiếp:** **V110**. Nếu sau này yêu cầu sửa phần mềm mà không chỉ định số phiên bản, áp dụng max + 1 = V111; **không tạo V111 trong lần cập nhật metadata này**.
- **Phạm vi xác nhận:** chung cho V110, chưa tách riêng CAD host. Các host trong hồ sơ lịch sử: AutoCAD 2022, AutoCAD 2025, GstarCAD 2027; chưa có bằng chứng người dùng xác nhận cụ thể host nào cho V110.
- **Bản kế thừa/nguồn gốc mã V110:** Chưa xác minh; không tự khẳng định là V105/V109.

## 2. Bằng chứng

| Mục | Nguồn | Kết quả |
| --- | --- | --- |
| Xác nhận người dùng | Phản hồi trong ChatGPT ngày 05/11/2026: “a đã cập nhật bản V110 build oke chạy test oke” | `UserReportedBuild=YES`, `UserReportedWorking=YES`, `UserReportedRuntime=YES` |
| ZIP trên nhánh chính | [DFrame-V110.zip](https://github.com/Tidi6969/DFrame/blob/main/DFrame-V110.zip) | **Có trên GitHub** (đối chiếu Git tree) |
| Kích thước ZIP | GitHub tree `main` | **7.456.590 byte** |
| Git blob SHA ZIP | GitHub tree `main` | `330ad9c72397910c06480d2f635d9d89df9c2f48` |
| Commit upload ZIP | [191701b7](https://github.com/Tidi6969/DFrame/commit/191701b7c8bff917cc7ac45c588af475bb1d56e0) | 05/11/2026 |
| Log build Windows theo host | Chưa được cung cấp/đối chiếu | `NotVerified` |
| NETLOAD, smoke test, UI theo host | Người dùng báo test OK chung; chưa có bảng host | `NotVerified` nếu yêu cầu chứng cứ riêng từng host |
| Nội dung ZIP, source, SDK, CRC, SHA-256 | Công cụ đọc GitHub tree chỉ xác minh đường dẫn/blob, chưa giải nén ZIP trong lần này | `NotVerified` |

## 3. Bảng đánh giá

| Tiêu chí | Trạng thái | Diễn giải |
| --- | --- | --- |
| Version V110 hiện có trên GitHub | **PASS** | Đã xác nhận tệp ZIP thực tế trên nhánh `main` |
| Người dùng xác nhận build thành công | **UserConfirmed** | Ghi nhận đúng phản hồi, chưa đối chiếu build log |
| Người dùng xác nhận chạy và kiểm thử thành công | **UserConfirmed** | Ghi nhận đúng phản hồi, không gán PASS riêng cho CAD host |
| Build PASS theo từng CAD host | **NotVerified** | Thiếu build log riêng từng host |
| Runtime/NETLOAD PASS theo từng CAD host | **NotVerified** | Chưa có danh sách host đã thử nghiệm |
| ZIP nội bộ, CRC, checksum SHA-256 | **NotVerified** | Chưa đọc lại nội dung ZIP |
| Standards STD-01–18 của mã nguồn V110 | **NotVerified** | Chưa phân tích source/structure của gói |
| Mục DFrame README và changelog | **Đã cập nhật** | Có hồ sơ V110 riêng trong repository DFrame |
| Mục DFrame trong DCAD | **Đã cập nhật** | Danh mục chỉ đến ZIP V110 và hồ sơ này |
| Tác động tới ZIP/source | **Không thay đổi** | Chỉ cập nhật metadata, không ghi đè ZIP hoặc tạo V111 |

## 4. Kiểm kê cây hiện hành và lịch sử

- Hiện trong `main`, **ZIP phiên bản duy nhất là `DFrame-V110.zip`**.
- Ngày 05/11/2026, chủ repository đã xóa `DFrame-V105.zip` và thư mục `V99/` khỏi cây `main` qua các commit riêng sau khi upload V110; các changelog V99 và V105 vẫn còn.
- Lịch sử Git các bản trước vẫn có thể truy cứu; **không ghi các ZIP đã xóa thành đường dẫn đang truy cập được trên `main`**.
- Không thay đổi hay phục hồi các file bị xóa khi thực hiện công việc cập nhật metadata này.

## 5. Điều kiện nâng mức đánh giá kỹ thuật trong tương lai

Để kết luận **Build PASS / NETLOAD PASS / Runtime PASS theo từng host**, cần có log build, phiên bản DLL và kết quả test cụ thể đối với từng host tương ứng. Để kết luận **Standards PASS** hoặc **ZIP verification PASS**, cần đọc cấu trúc source/SDK/ZIP và kiểm tra CRC hoặc checksum khi có thể. Trạng thái hiện tại không được tự động nâng lên chỉ từ việc có ZIP.

## 6. Liên kết lưu trữ

- [ZIP V110](https://github.com/Tidi6969/DFrame/blob/main/DFrame-V110.zip)
- [README DFrame](https://github.com/Tidi6969/DFrame/blob/main/README.md)
- [Changelog V110](https://github.com/Tidi6969/DFrame/blob/main/Change%20log/V110.txt)
- [Danh mục DCAD](https://github.com/Tidi6969/DCAD/blob/main/README.md)

**Nguyên tắc:** lưu dữ liệu đánh giá trung thực theo bằng chứng; phân biệt xác nhận của chủ dự án và kiểm chứng độc lập; đồng bộ thông tin, không sửa bản phát hành.
