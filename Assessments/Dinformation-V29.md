# Biên bản đánh giá Dinformation — V29

**Ngày đối chiếu:** 05/11/2026 (Asia/Bangkok)  
**Add-in:** Dinformation  
**Repository module:** [Tidi6969/Dinformation](https://github.com/Tidi6969/Dinformation)  
**Repository danh mục:** [Tidi6969/DCAD](https://github.com/Tidi6969/DCAD)  
**Quy định:** [Quy ước 17 — Autoupdate](https://github.com/Tidi6969/QuyUoc/blob/main/17_Autoupdate.md), mục 2.1, 8 và 9.

> Biên bản phân biệt bằng chứng ZIP thực tế trên GitHub với lời xác nhận theo ngữ cảnh của chủ dự án. Đây **không** phải báo cáo trợ lý đã trực tiếp build hoặc thử CAD.

## 1. Kết luận

- **Mới nhất đã lưu trên GitHub:** **V29**.
- **Trạng thái ghi nhận từ yêu cầu mới:** chủ dự án yêu cầu “tương tự https://github.com/Tidi6969/Dinformation”, kế tiếp yêu cầu “tương tự V105 ok” cho Dlayout. Yêu cầu này được **diễn giải theo ngữ cảnh** là muốn cập nhật đánh giá OK cho phiên bản V29 mới nhất. Không có câu xác nhận độc lập nêu đích danh V29 đã chạy thành công, không nêu CAD host cụ thể.
- **UserReportedWorking=YES (ContextInferred)**; đây là ghi nhận cách hiểu từ "tương tự", không tự nhận đã kiểm thử V29.
- **UserReportedBuild=NotSpecified**; lời yêu cầu không xác nhận build V29 cụ thể.
- **Baseline mặc định cho yêu cầu phát triển mới không chỉ định nguồn:** V29 theo STD-17, nhưng khi anh chỉ định V16 làm nguồn sửa một chức năng, phải ưu tiên chỉ định đó. Cần xác minh nội dung ZIP V29 trước khi phát triển.
- **Version đích mặc định khi thực sự sửa code:** V30; không tạo V30 trong lượt chỉ đồng bộ metadata.

## 2. Tình trạng ZIP thực tế

| Chỉ tiêu | Kết quả |
| --- | --- |
| ZIP mới nhất | [Dinformation-V29.zip](https://github.com/Tidi6969/Dinformation/blob/main/Dinformation-V29.zip) |
| Đường dẫn | `Dinformation-V29.zip` (root, branch `main`) |
| Dung lượng | **10.886.377 byte** |
| Git blob SHA | `30de9f8934c9e311455489d68fa60b7f65a7f509` |
| Commit upload | [8c206a4e](https://github.com/Tidi6969/Dinformation/commit/8c206a4e6a88042beb520937f0813f8e7feff734) |
| Bản cũ còn ZIP | V17, V18, V19, V20 (giữ nguyên) |
| ZIP source/CRC/SHA-256 V29 | `NotVerified` trong lần cập nhật này |

## 3. Bảng đánh giá theo bằng chứng

| Tiêu chí | Trạng thái | Giải thích |
| --- | --- | --- |
| ZIP V29 tồn tại trên GitHub | **PASS** | Có Git blob và dung lượng xác minh được |
| Chủ dự án đề nghị đồng bộ trạng thái giống Dlayout OK | **ContextInferred** | Yêu cầu “tương tự”, chưa xác nhận riêng V29 |
| Người dùng xác nhận build cụ thể V29 | **NotSpecified** | Không có phát biểu build V29 |
| Build từng CAD host | **NotVerified** | Chưa có log build V29 |
| NETLOAD/Runtime từng host | **NotVerified** | Chưa có bằng chứng chạy từng host V29 |
| Standards/SDK/source V29 | **NotVerified** | Chưa kiểm tra bên trong ZIP |
| CRC, SHA-256 V29 | **NotVerified** | Chưa mở/kiểm tra ZIP |
| README/changelog Dinformation | **Đã cập nhật** | Ghi V29 và lịch sử |
| Danh mục DCAD | **Đã cập nhật** | Mục Dinformation đổi mới nhất từ V20 lên V29 |
| Source/ZIP và các bản cũ | **Không thay đổi** | Chỉ cập nhật metadata |

**CAD target lịch sử từ V20:** AutoCAD 2022, AutoCAD 2025, GstarCAD 2018, GstarCAD 2027. Không suy diễn V29 đã build/test thành công riêng trên từng host.

## 4. Lịch sử chức năng, phiên bản đã nghiệm thu

- **V16:** Trước đó người dùng ưu tiên làm baseline về chức năng. ZIP V16 được cung cấp qua ChatGPT nhưng **chưa có trên nhánh main của repository này**. Điều đó không khẳng định V29 đã giữ đầy đủ hành vi V16.
- **V20:** Có ZIP đã lưu, hồ sơ ghi Build PASS bốn host nhưng NETLOAD/Runtime/Standards vẫn NotVerified; không sử dụng bằng chứng V20 để nâng V29 lên PASS.
- **V17, V18, V19, V20:** ZIP và changelog vẫn hiện diện. Không xóa hoặc ghi đè.
- **V29:** phiên bản ZIP mới nhất; chưa có kết quả đánh giá nội dung nguồn độc lập.

## 5. Tài liệu liên quan

- [ZIP V29](https://github.com/Tidi6969/Dinformation/blob/main/Dinformation-V29.zip)
- [README Dinformation](https://github.com/Tidi6969/Dinformation/blob/main/README.md)
- [Change log V29](https://github.com/Tidi6969/Dinformation/blob/main/Change%20log/V29.txt)
- [Danh mục DCAD](https://github.com/Tidi6969/DCAD/blob/main/README.md)

**Giới hạn:** Chỉ đánh giá trạng thái lưu trữ và ghi nhận yêu cầu. Muốn nâng Build/NETLOAD/Runtime của V29 lên PASS từng host cần log hoặc kết quả thử có phạm vi rõ ràng.
