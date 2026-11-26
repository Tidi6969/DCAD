# DCAD — Lộ trình bảo mật TidiDcad theo Sentinel LDK

**Ngày cập nhật:** 26/11/2026
**Baseline:** TidiDcad V55 — chủ dự án xác nhận chạy OK ("Oke 1 phát ăn luôn .", UserReportedWorking=YES).
**Hệ tham chiếu:** Thales Sentinel LDK; lấy Sentinel SL làm chuẩn chính cho bản quyền phần mềm offline, Envelope làm chuẩn mục tiêu bảo vệ chương trình. Sentinel HL/CL, network và các tính năng thương mại chỉ là tham chiếu mở rộng, không phải yêu cầu triển khai mặc định. Không tuyên bố tương đương mức bảo mật của Sentinel.
**Giai đoạn tiếp theo được chủ dự án chọn:** SEC-AT — Chống sửa Add-in (Program Integrity Protection).
**Quản trị:** [STD-18 V1.2](https://github.com/Tidi6969/QuyUoc/blob/main/18_Karpathy_Guidelines_cho_AI_lap_trinh.md), [STD-20 V1.2](https://github.com/Tidi6969/QuyUoc/blob/main/20_Quy_uoc_ban_giao_key_Addin.md), STD-17.

## 1. Ma trận năng lực và tiến độ

Trạng thái: **Có** = có theo thiết kế/triển khai V55 đã báo cáo, không mặc định đã nghiệm thu riêng; **Một phần** = có nền tảng nhưng thiếu phạm vi/cơ chế hoặc bằng chứng; **Chưa có** = chưa triển khai theo thông tin dự án hiện tại; **Chưa xác minh** = thiếu bằng chứng để kết luận; **Ngoài phạm vi** = không triển khai theo định hướng hiện tại. Nghiệm thu tách khỏi trạng thái có chức năng. Các mục dưới đây căn cứ lịch sử bàn giao V55 và xác nhận của chủ dự án, chưa rà lại toàn bộ source/binary hoặc chạy Windows/CAD trong lần cập nhật roadmap.

| ID | Năng lực tham chiếu Sentinel | DCAD V55 — hiện trạng | Trạng thái | Nghiệm thu / việc tiếp theo |
|---|---|---|---|---|
| LIC-01 | SL: cấp phép offline | DCAD_ID/dreq → LicenseccManager → Dcad.lic → Gate | Có | Xác nhận chung V55 OK; test luồng đầu-cuối riêng |
| LIC-02 | SL: khóa máy | DeviceID từ SMBIOS UUID, Gate đối chiếu máy | Có | Đúng/sai máy, phần cứng thay đổi; không coi là chống clone |
| LIC-03 | Feature và license terms | Tool/Feature XXX-YY, quyền và thời hạn riêng theo Feature | Có | Nghiệm thu một/nhiều Feature |
| LIC-04 | License xác thực, chống sửa dữ liệu cấp phép | Licensecc/Gate V2/V3; xác minh chữ ký và từ chối quyền sai | Có | Test License hợp lệ, bị sửa, thiếu, hết hạn |
| LIC-05 | Expiration / thời hạn | Kiểm tra thời gian UTC hệ thống | Có | Chưa đạt chuẩn chống lùi đồng hồ V-Clock |
| MGT-01 | Product/Feature/Entitlement management | Catalog và công cụ quản lý cấp phép | Một phần | Củng cố lịch sử cấp, khách hàng, audit và vòng đời quyền |
| MGT-02 | License update / renew | Có cấp License thay thế; luồng cập nhật/thu hồi/chuyển máy có kiểm soát chưa xác minh đầy đủ | Một phần | Quy trình cập nhật, gia hạn, phục hồi; chống replay |
| SEC-01 | Licensing API enforcement | DcadLicenseGate V6, ABI 2, Policy 1; Add-in chỉ ALLOW mới chạy nghiệp vụ | Có | Nghiệm thu mọi entry point từng Add-in |
| SEC-02 | Bảo vệ thành phần kiểm tra bản quyền | SEC06 xác minh chữ ký/hash Gate DLL trước nạp | Có | Nghiệm thu Gate thiếu/sai chữ ký/sai ABI, sai file |
| SEC-03 | Xác thực quy trình phát hành (năng lực bổ sung DCAD) | V55 ký RSA-PSS bộ Integration sáu file, xác thực lúc tiếp nhận | Có | Ký/xác minh PFX thật và chống sửa gói cần chứng cứ Windows riêng; không phải chống sửa binary Add-in |
| SEC-AT | Envelope Program Integrity Protection | Chưa có bảo vệ toàn vẹn chính ARX/DLL được nghiệm thu xuyên suốt | Chưa có | **Giai đoạn tiếp theo — đang khảo sát** |
| SEC-05 | Envelope Plus / obfuscation, anti-reverse engineering | Chưa có cơ chế chuyên dụng tương đương | Chưa có | Sau SEC-AT; chỉ nghiên cứu khi cần, không làm chậm CAD |
| SEC-06 | Bảo vệ mã đang chạy / chống can thiệp runtime | Gate kiểm tra file; không bảo đảm toàn vẹn mọi mã Add-in trong RAM | Một phần | Khảo sát độc lập sau bảo vệ file |
| SEC-07 | V-Clock / time tamper | Phụ thuộc đồng hồ hệ thống; chưa có thời gian tin cậy tương đương | Chưa có | Thiết kế chống lùi thời gian, phục hồi hợp lệ, giới hạn offline |
| SEC-08 | SL clone protection | Machine binding SMBIOS UUID; chưa có clone policy chuyên dụng | Một phần | Thử clone VM/snapshot, thay phần cứng và phục hồi |
| SEC-09 | Secure storage / bảo vệ trạng thái | Có quản lý khóa SEC06 và dữ liệu SQLite; chống rollback trạng thái, backup/restore chưa nghiệm thu đầy đủ | Một phần | Bảo toàn ToolCatalog, danh tính, backup đã xác minh; không reset dữ liệu thật khi build |
| SEC-10 | License revocation / rehost | Chưa có cơ chế thu hồi/chuyển quyền offline được xác minh đầy đủ | Chưa xác minh | Thiết kế vòng đời riêng; máy offline không nhận lệnh thu hồi tức thời |
| EXT-01 | Network/concurrency/detachable license | Không triển khai | Ngoài phạm vi | Khi phát sinh nhu cầu |
| EXT-02 | Cloud CL | Không triển khai | Ngoài phạm vi | Giữ offline |
| EXT-03 | HL hardware dongle | Không triển khai | Ngoài phạm vi | Không dùng USB theo định hướng đã duyệt |
| EXT-04 | Native/.NET protection và triển khai đa host | Hợp đồng được khảo sát native C++ AutoCAD 2022 x64; danh mục có thêm CAD nhưng chưa xác minh hợp đồng tương ứng | Một phần | AutoCAD 2025, GstarCAD 2027, C# từng hợp đồng riêng |

**Bằng chứng hiện tại:** UserReportedWorking=YES cho V55 ngày 26/11/2026. MSVC build log, ký/xác minh bằng PFX thực tế, Build/APPLOAD/Runtime của DJoin và Dtscr theo bộ bàn giao V55 vẫn NotVerified theo chứng cứ độc lập. Không dùng xác nhận chung hoặc kiểm tra Gate để đánh dấu SEC-AT PASS. Không dùng tỷ lệ phần trăm tương đương Sentinel.

## 2. Thứ tự phát triển

- Giai đoạn 1 — Nền tảng Licensecc, cấp quyền máy/Feature, SEC06 bảo vệ Gate, ký số bộ bàn giao: đã triển khai theo báo cáo; tiếp tục thu chứng cứ nghiệm thu.
- Giai đoạn 2 — **SEC-AT: chống sửa Add-in** (ưu tiên hiện tại, chủ dự án chọn).
- Giai đoạn 3 — Thời gian tin cậy và chống clone; bảo toàn dữ liệu/khóa là công việc song song xuyên suốt.
- Giai đoạn 4 — Bảo vệ mã chuyên sâu, hoàn thiện đa host và C# theo nhu cầu.
- Giai đoạn 5 — Vòng đời quyền, audit, gia hạn/thu hồi. Network/Cloud/USB chỉ xem xét theo yêu cầu riêng.

## 3. SEC-AT — Chống sửa Add-in: phạm vi khảo sát

**Mục tiêu:** phân biệt file Add-in chính thức đã phát hành với file bị sửa/thay thế; không cho phép nghiệp vụ được bảo vệ nếu kiểm tra toàn vẹn thất bại. Sentinel Envelope Program Integrity Protection là chuẩn năng lực mục tiêu, không sao chép công nghệ độc quyền.

Phân biệt ba đối tượng: Integration.zip (đã ký V55), Gate DLL (SEC06), chính thành phẩm Add-in (ARX/GRX/DLL — mục mới). Không nhầm chữ ký ZIP với chữ ký thành phẩm.

**Phương án đề xuất để đánh giá trước khi code:**
1. TidiDcad/đơn vị phát hành ký hoặc tạo manifest có chữ ký bao phủ binary cuối cùng, Tool/Feature, host, version và hash. Nghiên cứu tái sử dụng danh tính SEC06 hiện có với miền chữ ký riêng hoặc Authenticode nếu phù hợp hợp đồng chứng thư; không tự tạo khóa mới. Ký sau khi mọi bước thay đổi binary hoàn tất.
2. Ưu tiên xác minh bằng thành phần độc lập đã tin cậy trước khi nạp nếu host/quy trình triển khai hỗ trợ. Bảo toàn APPLOAD và cơ chế nạp CAD hợp lệ; nghiên cứu chính sách nạp và chữ ký Autodesk, không tự thay cấu hình Windows/CAD hoặc yêu cầu thêm phần mềm.
3. Nếu chỉ có kiểm tra trong Add-in/Gate sau khi nạp, phải ghi rõ hạn chế: kiểm tra nội bộ có thể bị sửa cùng mã và không bảo đảm chặn trước thực thi; không gọi đó là bảo vệ đầy đủ. Chữ ký trên đĩa không chứng minh toàn vẹn RAM; chữ ký số cũng không thay cho cơ chế cưỡng chế xác minh.
4. Thử nghiệm DJoin native AutoCAD 2022 x64 trước, dùng đúng baseline được xác nhận và bộ V55. Giữ Licensecc, Gate, Tool/Feature ID, License hiện hành, nghiệp vụ và Build_All gốc; không thêm lại ApprovedGateKeyId, PowerShell preflight, ExecutionPolicy hoặc phụ thuộc không cần thiết. Không mở rộng target/schema/Gate ABI nếu chưa duyệt tác động.
5. Tách giai đoạn bảo vệ file khỏi bảo vệ mã trong bộ nhớ, chống dịch ngược và chống debug. Chưa triển khai chống sửa runtime chuyên sâu trong giai đoạn đầu.

### Cổng nghiệm thu dự kiến (chưa chạy)

| ID | Ca thử | Expected |
|---|---|---|
| AT01 | Binary chính thức, đúng host, License hợp lệ | Nạp/chạy đúng nghiệp vụ |
| AT02 | Sửa byte của binary / thay bằng binary khác | Từ chối theo ranh giới xác minh đã thiết kế; không thực hiện nghiệp vụ |
| AT03 | Thiếu/sai chữ ký, sửa manifest, ký bằng danh tính khác | Từ chối an toàn |
| AT04 | Đúng file nhưng sai host/Tool/version theo hợp đồng | Từ chối hoặc báo lỗi tương thích đúng chính sách |
| AT05 | File thiếu/khóa/đọc lỗi, publish dở | Dừng an toàn; bảo toàn bản phát hành cũ |
| AT06 | File chính thức nhưng License sai/hết hạn/sai Feature/máy | Gate vẫn từ chối |
| AT07 | Build/APPLOAD/Runtime và Undo/Geometry/XData/Settings gốc | Không hồi quy; kiểm thử hiệu năng |
| AT08 | Kiểm tra đường nạp thực tế, mức cưỡng chế và thay đổi sau nạp | Ghi rõ giới hạn còn lại; không tuyên bố chặn trước thực thi nếu chưa có kiểm chứng |

Mỗi ca ghi Expected/Actual/Status/Host/Evidence theo AI-14–AI-18. Không sửa dữ liệu hoặc khóa thật để test. Chưa chọn thiết kế cuối, chưa sửa code, chưa tăng version. Quyết định phát triển và tiêu chí PASS phải được đối chiếu source V55, Gate client và nguồn DJoin thực tế trước khi triển khai.

## 4. Tài liệu chuẩn tham chiếu

- [Thales — Sentinel LDK](https://docs.sentinel.thalesgroup.com/softwareandservices/ldk/default.htm)
- [Thales — Sentinel LDK Protection: API và Envelope](https://docs.sentinel.thalesgroup.com/softwareandservices/ldk/LDKdocs/ldk-ems/SPNL/LDK_SLnP_Guide/Protection/Protecting_Software/Protection1.htm)
- [Thales — Windows protection settings / Program Integrity Protection](https://docs.sentinel.thalesgroup.com/ldk/LDKdocs/Env-Win/Windows/Win_NG_Default_Protection_Settings.htm)
- [Thales — Envelope Plus](https://docs.sentinel.thalesgroup.com/ldk/LDKdocs/Env-Win/Windows/Win_V3_envelope_plus_protection.htm)
- [Thales — Feature license terms](https://docs.sentinel.thalesgroup.com/softwareandservices/ldk/LDKdocs/ldk-ems/SPNL/LDK_SLnP_Guide/Licensing/Assigning_LicTerms.htm)
- [Thales — Offline activation](https://docs.sentinel.thalesgroup.com/softwareandservices/ldk/LDKdocs/ldk-ems/SPNL/LDK_SLnP_Guide/Licensing/KeyProtectionSL_Activation.htm)
- [Thales — V-Clock](https://docs.sentinel.thalesgroup.com/ldk/LDKdocs/SPNL/LDK_SLnP_Guide/Appendixes/HowProtects_TimeBased.htm)
- [Thales — Clone protection](https://docs.sentinel.thalesgroup.com/ldk/LDKdocs/SPNL/LDK_SLnP_Guide/Licensing/Managing_products/Clone_protection.htm)
- [Thales — Network concurrency](https://docs.sentinel.thalesgroup.com/softwareandservices/ldk/LDKdocs/ldk-ems/SPNL/LDK_SLnP_Guide/Models/LimitedConcurrent_EndUser.htm)
- [Thales — Client-side revocation](https://docs.sentinel.thalesgroup.com/softwareandservices/ldk/LDKdocs/SPNL/LDK_SLnP_Guide/Licensing/Client-Side_Lic_Revocation.htm)
- [Autodesk — Digitally signing custom program files](https://help.autodesk.com/cloudhelp/2025/ENU/AutoCAD-Customization/files/GUID-0A93626D-8389-45FC-969B-B86A2F37D691.htm)
- [Autodesk — SECURELOAD](https://help.autodesk.com/cloudhelp/2024/ENU/AutoCAD-Core/files/GUID-541566C6-2738-49DD-87C3-C1490E924A02.htm)

Đối chiếu tài liệu 26/11/2026. Năng lực Sentinel phụ thuộc loại khóa, phiên bản và gói bảo vệ; đây là chuẩn tham chiếu phát triển nội bộ, không phải chứng nhận Sentinel hoặc tuyên bố tương thích.

## 5. Lịch sử tiến độ

- 26/11/2026: V55 được chủ dự án xác nhận chạy OK; roadmap lấy Sentinel LDK làm chuẩn; chọn chống sửa Add-in làm giai đoạn tiếp theo. Chưa code giai đoạn SEC-AT. Giữ nguyên snapshot V55 và các quy ước đang hiệu lực.
