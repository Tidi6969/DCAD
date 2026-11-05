# Biên bản đánh giá Dlayout — V105

**Ngày đối chiếu:** 05/11/2026 (Asia/Bangkok)  
**Module:** Dlayout  
**Repository:** [Tidi6969/-Dlayout](https://github.com/Tidi6969/-Dlayout)  
**Kho tổng hợp:** [Tidi6969/DCAD](https://github.com/Tidi6969/DCAD)  
**Quy ước:** [STD-17](https://github.com/Tidi6969/QuyUoc/blob/main/17_Autoupdate.md) mục 2.1, 8 và 9.

> Đây là hồ sơ ghi nhận kết quả chủ dự án xác nhận và chứng cứ lưu trữ; không phải báo cáo AI tự build hoặc chạy thử CAD.

## 1. Kết quả và phạm vi

- **Mới nhất có ZIP trong `main`: V105.**
- **Bản chủ dự án xác nhận OK: V105.** Nguyên văn: “tương tự V105 ok https://github.com/Tidi6969/-Dlayout”.
- `UserReportedWorking=YES`; `UserReportedBuild=NotSpecified` vì người dùng chưa báo rõ riêng việc build V105.
- Baseline phát triển tiếp theo: V105, cần xác minh nội dung ZIP trước khi sửa.
- Version đích mặc định nếu sau này sửa code: V106; **không tạo V106** trong đợt đồng bộ này.

## 2. Chứng cứ GitHub

| Trường | Giá trị |
| --- | --- |
| ZIP V105 | [Dlayout-V105.zip](https://github.com/Tidi6969/-Dlayout/blob/main/Dlayout-V105.zip) |
| Đường dẫn | `Dlayout-V105.zip` tại root |
| Kích thước V105 | **9.375.720 byte** |
| Git blob V105 | `5a11ee45720f9de88bbedafe96b7233f8b8698bb` |
| Commit upload V105 | [de54d481](https://github.com/Tidi6969/-Dlayout/commit/de54d481c365df6e6fb919a008e8cd6b83986ade) |
| ZIP V102 | [V102/Dlayout-V102.zip](https://github.com/Tidi6969/-Dlayout/blob/main/V102/Dlayout-V102.zip) — **9.405.543 byte**, giữ nguyên |
| Kiểm tra ZIP CRC, SHA-256, source/SDK | `NotVerified` trong đợt metadata này |

## 3. Bảng đánh giá

| Nội dung | Trạng thái | Giải thích |
| --- | --- | --- |
| V105 ZIP tồn tại trên GitHub | **PASS** | Đối chiếu Git tree, kích thước và blob |
| Chủ dự án xác nhận V105 OK | **UserConfirmed** | `UserReportedWorking=YES` |
| Chủ dự án xác nhận build riêng V105 | **NotSpecified** | Chưa có thông tin build rõ ràng |
| Build PASS độc lập từng host | **NotVerified** | Không có build log V105 theo host |
| NETLOAD/Runtime PASS theo từng host | **NotVerified** | Chưa có danh sách host được thử |
| Standards STD-01–18 | **NotVerified** | Chưa audit source/SDK trong ZIP |
| ZIP nội bộ, CRC, SHA-256 | **NotVerified** | Chỉ kiểm chứng GitHub blob/size |
| README/changelog của Dlayout | **Đã cập nhật** | README và `Change log/V105.txt` |
| Danh mục DCAD | **Đã cập nhật** | Dlayout đổi V102 → V105 |
| Mã nguồn/ZIP | **Không thay đổi** | Không tạo V106, không xóa V102 |

**CAD target được ghi trong hồ sơ V102:** AutoCAD 2022, AutoCAD 2025, Desktop, GstarCAD 2027. Đây chỉ là danh sách lịch sử, không phải kết quả test của V105. Nguồn kỹ thuật tạo V105 chưa được xác minh.

## 4. Tài liệu

- [Dlayout V105 ZIP](https://github.com/Tidi6969/-Dlayout/blob/main/Dlayout-V105.zip)
- [README Dlayout](https://github.com/Tidi6969/-Dlayout/blob/main/README.md)
- [Changelog V105](https://github.com/Tidi6969/-Dlayout/blob/main/Change%20log/V105.txt)
- [Danh mục DCAD](https://github.com/Tidi6969/DCAD/blob/main/README.md)

**Giới hạn:** Chưa đủ chứng cứ để nâng `BuildStatus` / `NETLOAD` / `Runtime` riêng theo CAD host lên PASS hoặc công bố việc tuân thủ chuẩn source. 
