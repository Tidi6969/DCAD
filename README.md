# DCAD — Hệ thống quản lý Add-in CAD

**DCAD là repository tổng hợp trạng thái** của các Add-in; mỗi Add-in có repository riêng để lưu ZIP mã nguồn, DLL, changelog và lịch sử phiên bản. Không chép ZIP, SDK hoặc DLL của Add-in vào repository DCAD.

## Danh mục Add-in

| Add-in | Phiên bản mới nhất hiện có trên GitHub | Repository | ZIP | Trạng thái |
| --- | --- | --- | --- | --- |
| DBox | **V15** | [Tidi6969/DBox](https://github.com/Tidi6969/DBox) | [DBox-V15.zip](https://github.com/Tidi6969/DBox/blob/main/DBox-V15.zip) | **Bản mới nhất đã lưu / baseline / bản chủ dự án xác nhận chạy OK: V15** (05/11/2026, `UserReportedWorking=YES`). `BuildStatus=NotVerified` và `NETLOAD/RuntimeStatus=NotVerified` theo từng CAD host do chưa có log/test tách host; `StandardsStatus=NotVerified` (chưa đọc nội dung ZIP). CAD target lịch sử: AutoCAD2022, AutoCAD2025, GstarCAD2027, không coi đó là phạm vi V15 đã được xác minh. ZIP V15 ở thư mục gốc, 6.646.961 byte, Git blob `20b06f6544036527242a6a83c97f47b1c170489c`; nội dung/CRC/SHA-256 chưa kiểm tra. ZIP V4 đã được chủ repo xóa khỏi `main` ngày 05/11 nhưng changelog V4/lịch sử Git còn. [Changelog V15](https://github.com/Tidi6969/DBox/blob/main/Change%20log/V15.txt) · [Biên bản đánh giá V15](https://github.com/Tidi6969/DCAD/blob/main/Assessments/DBox-V15.md). Lần này chỉ đồng bộ metadata, không sửa ZIP/code hoặc tạo V16 |
| DPunch | V390 | [Tidi6969/Dpunch](https://github.com/Tidi6969/Dpunch) | [DPunch-V390.zip](https://github.com/Tidi6969/Dpunch/blob/main/V390/DPunch-V390.zip) | Snapshot nguồn gốc; chủ dự án duyệt làm baseline; Build/Runtime: NotVerified; CAD target: chưa xác minh; đồng bộ 31/10/2026 |
| DCPart | V55 | [Tidi6969/DCPart](https://github.com/Tidi6969/DCPart) | [DCPart-V55.zip](https://github.com/Tidi6969/DCPart/blob/main/V55/DCPart-V55.zip) | Snapshot nguồn gốc; Build/Runtime: NotVerified; target dự án: AutoCAD2022, AutoCAD2025, GstarCAD2027; ZIP CRC PASS và Git blob khớp nguồn; đồng bộ 02/11/2026 |
| DClean | V1 | [Tidi6969/DClean](https://github.com/Tidi6969/DClean) | [DClean-V1.zip](https://github.com/Tidi6969/DClean/blob/main/V1/DClean-V1.zip) | Snapshot nguồn gốc; Build/Runtime: NotVerified; target dự án: AutoCAD2022; ZIP CRC và Git blob khớp nguồn; đồng bộ 31/10/2026 |
| DET-DEM-DEA | V17 | [Tidi6969/-DET-DEM-DEA](https://github.com/Tidi6969/-DET-DEM-DEA) | [DET-DEM-DEA-V17.zip](https://github.com/Tidi6969/-DET-DEM-DEA/blob/main/V17/DET-DEM-DEA-V17.zip) | Snapshot nguồn gốc; Build/Runtime: NotVerified; target dự án: AutoCAD2022, AutoCAD2025, GstarCAD2018, GstarCAD2027; ZIP CRC và Git blob khớp nguồn; đồng bộ 31/10/2026 |
| DFrame | **V112** | [Tidi6969/DFrame](https://github.com/Tidi6969/DFrame) | [DFrame-V112.zip](https://github.com/Tidi6969/DFrame/blob/main/DFrame-V112.zip) | **Mới nhất đã lưu / baseline / bản ghi nhận nghiệm thu theo yêu cầu tương tự DProject: V112** (05/11/2026; `UserReportedBuild=YES`, `UserReportedWorking=YES`, `UserReportedRuntime=YES` theo ngữ cảnh người dùng yêu cầu “Tương tự” ngay sau xác nhận DProject V17 build/chạy OK). Chưa có kết quả riêng theo CAD host: Build/NETLOAD/Runtime PASS từng host = `NotVerified` về chứng cứ độc lập; `StandardsStatus=NotVerified` và ZIP CRC chưa kiểm tra. CAD target lịch sử AutoCAD2022, AutoCAD2025, GstarCAD2027 (không suy diễn đã test từng host ở V112). ZIP V112 có tại root, 7.467.098 byte, Git blob `07c9dde40e7689711011e0cbce63069a1cdd559d`. ZIP V110 bị xóa khỏi `main` trước khi V112 được upload; changelog V110 và các changelog cũ vẫn có. [Changelog V112](https://github.com/Tidi6969/DFrame/blob/main/Change%20log/V112.txt) · [Biên bản đánh giá V112](https://github.com/Tidi6969/DCAD/blob/main/Assessments/DFrame-V112.md). Chỉ cập nhật metadata, không sửa ZIP/source hoặc tạo V113 |
| DJoin | V14 | [Tidi6969/Djoin](https://github.com/Tidi6969/Djoin) | [DJoin-V14.zip](https://github.com/Tidi6969/Djoin/blob/main/V14/DJoin-V14.zip) | Snapshot nguồn gốc; Build/Runtime: NotVerified; target dự án: AutoCAD2022, AutoCAD2025, GstarCAD2027; ZIP CRC và Git blob khớp nguồn; đồng bộ 31/10/2026 |
| DNesting | V49 | [Tidi6969/-DNesting](https://github.com/Tidi6969/-DNesting) | [DNesting-V49.zip](https://github.com/Tidi6969/-DNesting/blob/main/V49/DNesting-V49.zip) | Đã lưu ZIP nguyên gói; Git blob và kích thước khớp biên bản nguồn; CRC nguồn PASS; target dự án: AutoCAD2022, AutoCAD2025, GstarCAD2027, Desktop; Build/Runtime: NotVerified; đối chiếu 02/11/2026 |
| DProject | **V17** | [Tidi6969/DProject](https://github.com/Tidi6969/DProject) | [DProject-V17.zip](https://github.com/Tidi6969/DProject/blob/main/DProject-V17.zip) | **Mới nhất đã lưu / baseline / bản chủ dự án xác nhận build và chạy thử OK: V17** (05/11/2026; `UserReportedBuild=YES`, `UserReportedWorking=YES`, `UserReportedRuntime=YES`). Chưa nêu CAD host đã thử nên `Build/NETLOAD/Runtime PASS` tách từng host = `NotVerified` khi cần bằng chứng độc lập. `StandardsStatus=NotVerified` và CRC/nội dung ZIP chưa kiểm tra. Các target lịch sử: AutoCAD2022, AutoCAD2025, GstarCAD2027; không suy ra V17 đã thử đủ 3 host. ZIP V17 tồn tại ở root, 6.668.493 byte, Git blob `8f72bc7b9401bb7018dbb0dd8455b6ad60761e7f`. ZIP V12/V13 đã được xóa khỏi `main`, changelog cũ vẫn giữ. [Changelog V17](https://github.com/Tidi6969/DProject/blob/main/Change%20log/V17.txt) · [Biên bản đánh giá V17](https://github.com/Tidi6969/DCAD/blob/main/Assessments/DProject-V17.md). Chỉ cập nhật metadata, không sửa ZIP/source hoặc tạo V18 |
| DTrimView | **V29 (mới nhất có ZIP trên GitHub)** | [Tidi6969/DTrimView](https://github.com/Tidi6969/DTrimView) | [DTrimView-V29.zip](https://github.com/Tidi6969/DTrimView/blob/main/V29/DTrimView-V29.zip) | Snapshot nguồn gốc V29 còn nguyên, ZIP CRC PASS và Git blob khớp nguồn. **V31: chủ dự án phản hồi “oke rồi” với gói mã nguồn bàn giao qua ChatGPT ngày 05/11/2026** (`UserAcceptedPackage=YES`; không phải xác nhận build/chạy CAD). V31 chưa có ZIP trên GitHub, không được coi là phiên bản đã lưu/phát hành. `BuildStatus=NotVerified`, `NETLOAD/RuntimeStatus=NotVerified`, `StandardsStatus=NotVerified`; không có kết quả độc lập cho AutoCAD2022, AutoCAD2025, GstarCAD2027. Đồng bộ metadata 05/11/2026; không chỉnh ZIP/source hoặc tạo V31 trên GitHub |
| Dcenterline | V32 | [Tidi6969/-Dcenterline](https://github.com/Tidi6969/-Dcenterline) | [Dcenterline-V32.zip](https://github.com/Tidi6969/-Dcenterline/blob/main/V32/Dcenterline-V32.zip) | Snapshot nguồn gốc; Build/Runtime: NotVerified; target dự án: AutoCAD2022, AutoCAD2025, GstarCAD2027; ZIP CRC và Git blob khớp nguồn; đồng bộ 31/10/2026 |
| Dcorner | **V26 (mới nhất có ZIP trên GitHub)**; **V38 (chủ dự án xác nhận chạy tốt)** | [Tidi6969/Dcorner](https://github.com/Tidi6969/Dcorner) | [Dcorner-V26.zip](https://github.com/Tidi6969/Dcorner/blob/main/V26/Dcorner-V26.zip) | **V38: chủ dự án phản hồi “oke ngon rồi” ngày 09/11/2026** (`UserReportedWorking=YES`) sau khi sửa Loại 5 để chọn cạnh chuẩn/offset H và xử lý góc không vuông. Phạm vi xác nhận là hành vi người dùng đã thử; CAD host cụ thể chưa được nêu. `BuildStatus/NETLOADStatus/RuntimeStatus` riêng AutoCAD2022, AutoCAD2025, GstarCAD2027 = `NotVerified` theo bằng chứng độc lập; `StandardsStatus=NotVerified`. V38 mới có ZIP trong ChatGPT Library (`/Dcorner/Dcorner-V38.zip`), **chưa có ZIP trên GitHub**, không xem là bản đã phát hành. V26 vẫn là ZIP mới nhất trên GitHub, snapshot gốc/CRC PASS, được giữ nguyên. **Chỉ cập nhật metadata nghiệm thu; không sửa ZIP/source, không tự tạo V39.** [Thông tin V38](https://github.com/Tidi6969/Dcorner/blob/main/README.md) |
| Dinformation | **V29** | [Tidi6969/Dinformation](https://github.com/Tidi6969/Dinformation) | [Dinformation-V29.zip](https://github.com/Tidi6969/Dinformation/blob/main/Dinformation-V29.zip) | **Mới nhất đã lưu / baseline mặc định cho yêu cầu phát triển mới không chỉ định nguồn: V29** (05/11/2026). Chủ dự án yêu cầu “tương tự” ngay sau Dlayout V105 OK, nên ghi nhận `UserReportedWorking=YES (ContextInferred)` cho V29; đây là suy luận theo ngữ cảnh, **chưa phải xác nhận trực tiếp V29 đã chạy/test trên từng host**. `UserReportedBuild=NotSpecified`; Build/NETLOAD/Runtime mỗi CAD host=`NotVerified`, Standards/CRC/ZIP content=`NotVerified`. CAD target lịch sử theo V20: AutoCAD2022, AutoCAD2025, GstarCAD2018, GstarCAD2027 (không áp PASS V20 sang V29). ZIP V29 ở root, 10.886.377 byte, Git blob `30de9f8934c9e311455489d68fa60b7f65a7f509`. **Lịch sử:** Chủ dự án từng ưu tiên V16 làm baseline chức năng; ZIP V16 không nằm trên GitHub, không suy V29 có cùng hành vi. ZIP V17/V18/V19/V20 còn nguyên. [Changelog V29](https://github.com/Tidi6969/Dinformation/blob/main/Change%20log/V29.txt) · [Biên bản đánh giá V29](https://github.com/Tidi6969/DCAD/blob/main/Assessments/Dinformation-V29.md). Chỉ sửa metadata, không tạo V30 hoặc sửa ZIP/source |
| Dlayout | **V105** | [Tidi6969/-Dlayout](https://github.com/Tidi6969/-Dlayout) | [Dlayout-V105.zip](https://github.com/Tidi6969/-Dlayout/blob/main/Dlayout-V105.zip) | **Mới nhất đã lưu / baseline / bản chủ dự án xác nhận OK: V105** (05/11/2026; `UserReportedWorking=YES`, lời xác nhận “tương tự V105 ok”). Không có xác nhận build riêng V105 (`UserReportedBuild=NotSpecified`); `Build/NETLOAD/RuntimeStatus` từng CAD host = `NotVerified` theo bằng chứng độc lập, `StandardsStatus=NotVerified`, CRC/nội dung ZIP chưa được kiểm tra. CAD target lịch sử của V102: AutoCAD2022, AutoCAD2025, Desktop, GstarCAD2027 (không coi đây là bằng chứng V105 đã được test đủ 4 host). ZIP V105 thực tế nằm ở root, 9.375.720 byte, Git blob `5a11ee45720f9de88bbedafe96b7233f8b8698bb`. V102 còn được lưu tại `V102/Dlayout-V102.zip` và giữ nguyên. [Changelog V105](https://github.com/Tidi6969/-Dlayout/blob/main/Change%20log/V105.txt) · [Biên bản đánh giá V105](https://github.com/Tidi6969/DCAD/blob/main/Assessments/Dlayout-V105.md). Đồng bộ 05/11/2026; không sửa ZIP/source, không tạo V106 |
| Dpdf+Dprint | V135 | [Tidi6969/Dpdf-Dprint](https://github.com/Tidi6969/Dpdf-Dprint) | [Dpdf+Dprint-V135.zip](https://github.com/Tidi6969/Dpdf-Dprint/blob/main/V135/Dpdf%2BDprint-V135.zip) | Snapshot nguồn gốc; Build/Runtime: NotVerified; target dự án: AutoCAD2022, AutoCAD2025, GstarCAD2018, GstarCAD2027, DPDF (Desktop); ZIP CRC PASS và Git blob khớp nguồn; đồng bộ 02/11/2026 |
| Dsplit | V203 | [Tidi6969/Dsplit](https://github.com/Tidi6969/Dsplit) | [Dsplit-V203.zip](https://github.com/Tidi6969/Dsplit/blob/main/V203/Dsplit-V203.zip) | Đã lưu ZIP nguyên gói; Git blob và kích thước khớp biên bản nguồn; CRC nguồn PASS; target dự án: AutoCAD2022, AutoCAD2025, GstarCAD2027; Build/Runtime: NotVerified; đối chiếu 02/11/2026 |
| Dtag | V54 | [Tidi6969/-Dtag](https://github.com/Tidi6969/-Dtag) | [Dtag-V54.zip](https://github.com/Tidi6969/-Dtag/blob/main/V54/Dtag-V54.zip) | Snapshot nguồn gốc; Build/Runtime: NotVerified; target dự án: AutoCAD2022, AutoCAD2025, GstarCAD2018, GstarCAD2027; ZIP CRC và Git blob khớp nguồn; đồng bộ 31/10/2026 |

**Đối chiếu kho ngày 31/10/2026:** đã kiểm tra sự tồn tại của các đường dẫn ZIP nêu trong bảng qua cây file GitHub. Việc một file ZIP tồn tại **không** chứng minh build thành công hay NETLOAD/runtime đã PASS.

## DPunch V390 — thông tin lưu trữ

- **Bản chuẩn:** V390, được chủ dự án chấp thuận để lưu trữ và làm nền cải tiến ngày 31/10/2026 (Asia/Bangkok). Giữ nguyên ZIP và changelog gốc.
- **Loại bản:** snapshot nguồn gốc, chưa xác minh build; không công bố là bản phát hành đã nghiệm thu CAD.
- **BuildStatus / RuntimeStatus / StandardsStatus:** `NotVerified`. Changelog gốc chưa xác nhận build Windows, NETLOAD hoặc kiểm thử UI; lời duyệt lưu trữ không xác định kết quả kiểm thử trên từng CAD.
- **CAD target trong gói:** `NotVerified` — chưa đọc được nội dung ZIP; không suy từ các target tiêu chuẩn của hệ thống.
- **Kiểm tra lưu trữ:** ZIP tồn tại trên GitHub, 11.063.361 byte, Git blob SHA `c2251dcee0b32d389b34f5e4bfbfe39a0c33cea0`. Nội dung ZIP/CRC/SHA-256: `NotVerified` do công cụ hiện có chưa trả được dữ liệu ZIP.
- **Liên kết:** [ZIP V390](https://github.com/Tidi6969/Dpunch/blob/main/V390/DPunch-V390.zip) · [Changelog](https://github.com/Tidi6969/Dpunch/blob/main/Change%20log/V390.txt) · [Biên bản lưu trữ](https://github.com/Tidi6969/Dpunch/blob/main/V390/ArchiveInfo.json).
- **Ngày đồng bộ:** 31/10/2026 (Asia/Bangkok). Phiên bản mới nhất đã lưu vẫn là V390; chưa sửa mã nguồn, tăng phiên bản hoặc build lại.

## Mục tiêu CAD

Các target tiêu chuẩn của hệ thống là **AutoCAD 2022, AutoCAD 2025 và GstarCAD 2027**, nhưng phạm vi build/kiểm thử của từng phiên bản phải dựa trên log và chứng cứ riêng; không suy từ danh sách target tiêu chuẩn.

## Quy trình giao việc và tự đồng bộ

1. Chủ dự án giao yêu cầu sửa code hoặc phiên bản mới **tại ChatGPT**. Ưu tiên baseline/version chỉ định; nếu không chỉ định bản gốc thì tự lấy phiên bản gần nhất đã lưu của đúng module trên GitHub, nếu không chỉ định version đích thì tăng số lớn nhất đã lưu đúng 1 (V49 → V50). CAD mục tiêu dùng phạm vi đã giao/thống nhất; giữ các bản cũ và ghi riêng bản mới nhất với bản đã nghiệm thu theo STD-01/17. Chỉ lưu nguyên bản hoặc đồng bộ metadata không tự tăng version phần mềm.
2. Trợ lý đọc mã nguồn gốc, chỉ sửa nội dung được yêu cầu, kiểm tra cấu trúc, build và QA đúng khả năng môi trường. Khi chưa chạy build/CAD thực tế phải ghi **NotVerified**, không tuyên bố PASS.
3. Chỉ khi đạt điều kiện phát hành của [DCAD-STD-17 — Autoupdate](https://github.com/Tidi6969/QuyUoc/blob/main/17_Autoupdate.md), tự đóng gói và upload ZIP cùng changelog vào repository Add-in; nếu chỉ được yêu cầu lưu snapshot nguồn, phải ghi đúng loại bản.
4. **Sau khi xác minh ZIP đã có trên GitHub**, tự cập nhật danh mục DCAD: tên Add-in, phiên bản mới nhất, trạng thái build/runtime, CAD target và link ZIP/changelog khi phù hợp. Việc này thuộc ủy quyền của yêu cầu phát hành, **không cần xác nhận upload lần hai**.
5. Đọc lại GitHub module và DCAD; khi hoàn tất, trả một link GitHub `/blob/main/<path-to-zip>`. Nếu có lỗi build, upload hoặc đồng bộ, báo rõ trạng thái từng bước, không gửi link giả hay gọi bản chưa hoàn tất là bản đã phát hành.
6. Chủ dự án **tải ZIP về máy và chạy thử CAD**, phản hồi kết quả/lỗi tại ChatGPT. Khi có kết quả thử thực tế, cập nhật đúng trạng thái; nếu cần sửa thì tạo phiên bản theo yêu cầu, không ghi đè phiên bản cũ.

**Luồng chuẩn:** ChatGPT → repository Add-in → danh mục DCAD → link ZIP → chạy thử tại máy người dùng → phản hồi tại ChatGPT.

## Phân biệt trạng thái

- **Đã lưu ZIP:** tệp tồn tại trên GitHub; không đồng nghĩa đã build/kiểm thử.
- **Build PASS:** có bằng chứng biên dịch/publish thành công trên đúng host CAD.
- **Runtime PASS:** đã NETLOAD/thử chức năng trên CAD tương ứng và có bằng chứng.
- **NotVerified:** chưa có đủ kiểm chứng, không được đổi thành PASS theo suy đoán.
- **Chưa đồng bộ DCAD:** repository module có bản mới nhưng mục thông tin tổng hợp còn thiếu hoặc cũ; phải báo rõ.

## Quy chuẩn

Áp dụng bộ quy ước tại [Tidi6969/QuyUoc](https://github.com/Tidi6969/QuyUoc), đặc biệt [17_Autoupdate.md](https://github.com/Tidi6969/QuyUoc/blob/main/17_Autoupdate.md) về tự động cập nhật module và DCAD.

**Bộ quy ước hiện hành: V1.12 — 03/11/2026.** [Tải ZIP quy ước V1.12](https://github.com/Tidi6969/QuyUoc/blob/main/Releases/V1.12/QuyUoc-V1.12.zip). STD-05: tên thư mục cuối của entry Support Path phải khớp DData/DUser/DProgram/Dicon/Dhelp; không bắt đủ năm, cùng root hoặc vị trí cuối danh sách. Chỉ kiểm tài nguyên thực sự cần dùng; đường dẫn con ứng dụng phải khai báo riêng, ví dụ DProgram\Dnest\Dnest.exe. Lần cập nhật này chỉ sửa quy ước và metadata, không sửa hoặc build lại các Add-in.

## Chủ sở hữu

GitHub: [Tidi6969](https://github.com/Tidi6969)


## Ứng dụng độc lập đang phát triển (không phải add-in CAD)

| Ứng dụng | Phiên bản nguồn/toolkit | Repository | ZIP | Trạng thái |
| --- | --- | --- | --- | --- |
| DfreeCad | **V12-update** — sửa build tăng dần và cập nhật DProgram an toàn | [Tidi6969/DfreeCad](https://github.com/Tidi6969/DfreeCad) | [DfreeCad-V12-Update.zip](https://github.com/Tidi6969/DfreeCad/releases/download/V12-update/DfreeCad-V12-Update.zip) | **Mới nhất đã lưu: V12 (11/11/2026)** — ZIP cập nhật 5.699 byte, SHA256 `e168d17b2545b4f6a6c46e5e64a6a84cc7d28dd502cafdc0dc4509d1a9469979`. **Nguồn đầy đủ V9** ([ZIP V9](https://github.com/Tidi6969/DfreeCad/releases/download/V9-fullsource/DfreeCad-V9-FullSource-BuildKit.zip)) + cập nhật V10 (compiler) và V11 (Measurement). Log người dùng `Build-20261111-160857.log`: MSVC 14.30+NMake PASS; V10 từ chối `DProgram\DfreeCad` có sẵn trước CMake. V12 tạo Build-V12.ps1, giữ build cache, staging riêng; sau khi kiểm tra EXE mới thành công, sao lưu DProgram cũ và thay bản mới. **QA áp dụng nguồn/ZIP và mô phỏng thay cũ, giữ backup, từ chối staging thiếu file=PASS** ([Windows CI](https://github.com/Tidi6969/DfreeCad/actions/runs/42994081641)); **rollback khi lỗi ở giữa bước chuyển bản=NotVerified**; **Build thực tế/Runtime Measurement=NotVerified**, **nghiệm thu người dùng=NotVerified**. Gói cập nhật nguồn, chưa có EXE được xác nhận. |
| TidiDcad | **V55** — baseline được chủ dự án xác nhận OK | Chưa xác định kho module riêng trong danh sách kho được cấp quyền | Chưa xác minh ZIP trên GitHub | **26/11/2026: chủ dự án phản hồi “Oke 1 phát ăn luôn .”** (`UserReportedWorking=YES`), sau bàn giao V55. Baseline phát triển tiếp: V55 (từ V54). Ký số Integration RSA-PSS, xác thực khi tiếp nhận; bỏ phê duyệt máy build và preflight phê duyệt PowerShell theo [STD-20 V1.2](https://github.com/Tidi6969/QuyUoc/blob/main/20_Quy_uoc_ban_giao_key_Addin.md), giữ sáu file, Gate/Licensecc. Build log MSVC, ca ký/xác minh PFX thực tế, kiểm thử từng chức năng Windows và nghiệm thu DJoin/Dtscr trên CAD: `NotVerified` theo chứng cứ độc lập; phạm vi hợp đồng tích hợp native C++ AutoCAD 2022 x64. Không coi xác nhận chung là PASS mọi ca. Giai đoạn phát triển tiếp theo: **chống sửa Add-in (SEC-AT)**, lấy Sentinel LDK làm chuẩn năng lực; nghiệm thu Integration mới với DJoin/Dtscr vẫn là cổng kiểm chứng. Xem bảng tiến độ bảo mật TidiDcad ngay bên dưới.. Chỉ ghi nhận tiến độ; không sửa source, không tạo V56, không upload ZIP. |

### Tiến độ bảo mật TidiDcad — Sentinel LDK

**Ngày cập nhật:** 26/11/2026
**Baseline:** TidiDcad V55 — chủ dự án xác nhận chạy OK ("Oke 1 phát ăn luôn .", UserReportedWorking=YES).
**Hệ tham chiếu:** Thales Sentinel LDK; lấy Sentinel SL làm chuẩn chính cho bản quyền phần mềm offline, Envelope làm chuẩn mục tiêu bảo vệ chương trình. Sentinel HL/CL, network và các tính năng thương mại chỉ là tham chiếu mở rộng, không phải yêu cầu triển khai mặc định. Không tuyên bố tương đương mức bảo mật của Sentinel.
**Giai đoạn tiếp theo được chủ dự án chọn:** SEC-AT — Chống sửa Add-in (Program Integrity Protection).
**Quản trị:** [STD-18 V1.2](https://github.com/Tidi6969/QuyUoc/blob/main/18_Karpathy_Guidelines_cho_AI_lap_trinh.md), [STD-20 V1.2](https://github.com/Tidi6969/QuyUoc/blob/main/20_Quy_uoc_ban_giao_key_Addin.md), STD-17.

#### 1. Ma trận năng lực và tiến độ

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

#### 2. Thứ tự phát triển

- Giai đoạn 1 — Nền tảng Licensecc, cấp quyền máy/Feature, SEC06 bảo vệ Gate, ký số bộ bàn giao: đã triển khai theo báo cáo; tiếp tục thu chứng cứ nghiệm thu.
- Giai đoạn 2 — **SEC-AT: chống sửa Add-in** (ưu tiên hiện tại, chủ dự án chọn).
- Giai đoạn 3 — Thời gian tin cậy và chống clone; bảo toàn dữ liệu/khóa là công việc song song xuyên suốt.
- Giai đoạn 4 — Bảo vệ mã chuyên sâu, hoàn thiện đa host và C# theo nhu cầu.
- Giai đoạn 5 — Vòng đời quyền, audit, gia hạn/thu hồi. Network/Cloud/USB chỉ xem xét theo yêu cầu riêng.

#### 3. SEC-AT — Chống sửa Add-in: phạm vi khảo sát

**Mục tiêu:** phân biệt file Add-in chính thức đã phát hành với file bị sửa/thay thế; không cho phép nghiệp vụ được bảo vệ nếu kiểm tra toàn vẹn thất bại. Sentinel Envelope Program Integrity Protection là chuẩn năng lực mục tiêu, không sao chép công nghệ độc quyền.

Phân biệt ba đối tượng: Integration.zip (đã ký V55), Gate DLL (SEC06), chính thành phẩm Add-in (ARX/GRX/DLL — mục mới). Không nhầm chữ ký ZIP với chữ ký thành phẩm.

**Phương án đề xuất để đánh giá trước khi code:**
1. TidiDcad/đơn vị phát hành ký hoặc tạo manifest có chữ ký bao phủ binary cuối cùng, Tool/Feature, host, version và hash. Nghiên cứu tái sử dụng danh tính SEC06 hiện có với miền chữ ký riêng hoặc Authenticode nếu phù hợp hợp đồng chứng thư; không tự tạo khóa mới. Ký sau khi mọi bước thay đổi binary hoàn tất.
2. Ưu tiên xác minh bằng thành phần độc lập đã tin cậy trước khi nạp nếu host/quy trình triển khai hỗ trợ. Bảo toàn APPLOAD và cơ chế nạp CAD hợp lệ; nghiên cứu chính sách nạp và chữ ký Autodesk, không tự thay cấu hình Windows/CAD hoặc yêu cầu thêm phần mềm.
3. Nếu chỉ có kiểm tra trong Add-in/Gate sau khi nạp, phải ghi rõ hạn chế: kiểm tra nội bộ có thể bị sửa cùng mã và không bảo đảm chặn trước thực thi; không gọi đó là bảo vệ đầy đủ. Chữ ký trên đĩa không chứng minh toàn vẹn RAM; chữ ký số cũng không thay cho cơ chế cưỡng chế xác minh.
4. Thử nghiệm DJoin native AutoCAD 2022 x64 trước, dùng đúng baseline được xác nhận và bộ V55. Giữ Licensecc, Gate, Tool/Feature ID, License hiện hành, nghiệp vụ và Build_All gốc; không thêm lại ApprovedGateKeyId, PowerShell preflight, ExecutionPolicy hoặc phụ thuộc không cần thiết. Không mở rộng target/schema/Gate ABI nếu chưa duyệt tác động.
5. Tách giai đoạn bảo vệ file khỏi bảo vệ mã trong bộ nhớ, chống dịch ngược và chống debug. Chưa triển khai chống sửa runtime chuyên sâu trong giai đoạn đầu.

##### Cổng nghiệm thu dự kiến (chưa chạy)

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

#### 3A. Phương pháp nghiên cứu và phát triển SEC-AT — Sentinel làm chuẩn, mã nguồn mở làm cơ sở

**Đã được chủ dự án duyệt ngày 26/11/2026.** Lấy tài liệu công khai của Sentinel LDK Envelope (ưu tiên Windows V3 Engine cho native ARX) làm chuẩn kiến trúc, năng lực và tiêu chí đánh giá. Tìm các dự án mã nguồn mở, đặc tả và API hệ điều hành tương ứng từng năng lực để phát triển độc lập; không sao chép mã hay suy đoán thuật toán độc quyền của Thales. Tạm gọi lớp bảo vệ mục tiêu là DcadEnvelope, chưa quyết định cấu trúc đóng gói hoặc tạo ứng dụng/EXE riêng. Giữ V55, Licensecc, SEC06, quy trình cấp phép offline và STD-20 hiện hành.

##### Ma trận ứng viên mã nguồn và công nghệ

| Mã nghiên cứu | Năng lực mục tiêu | Nguồn ứng viên | Vai trò, giới hạn | Trạng thái |
|---|---|---|---|---|
| REF-01 | Phân tích binary PE/ARX/DLL | [LIEF](https://github.com/lief-project/LIEF), [Microsoft PE Format](https://learn.microsoft.com/en-us/windows/win32/debug/pe-format) | Đọc cấu trúc và dữ liệu chữ ký; không phải Anti-Tamper hoàn chỉnh | Chờ khảo sát/build nguyên bản |
| REF-02 | File/Program Integrity Protection | [Authenticode](https://learn.microsoft.com/en-us/windows/win32/secbp/understanding-pe-signatures), [osslsigncode](https://github.com/mtrojnar/osslsigncode), [fs-verity](https://docs.kernel.org/filesystems/fsverity.html) | Ký/xác minh PE; tham khảo hash theo khối. fs-verity là cơ chế Linux, không đưa nguyên kernel sang Windows | Chờ kiểm chứng |
| REF-03 | Code Encryption | [OpenSSL](https://github.com/openssl/openssl) | Thành phần mật mã tiêu chuẩn, không phải engine bảo vệ mã thực thi; ưu tiên tận dụng thư viện/API đã có nếu đủ | Chờ đánh giá nhu cầu |
| REF-04 | Code Transformation / Obfuscation | [LLVM](https://github.com/llvm/llvm-project) | Hạ tầng compiler/IR; không có sẵn Envelope Plus của Thales | Nghiên cứu sau SEC-AT cơ bản |
| REF-05 | Runtime / Section Integrity | [fsverity-utils](https://github.com/ebiggers/fsverity-utils), [Tigress Integrity](https://tigress.wtf/integrity.html) | Học nguyên lý; hash file không đồng nghĩa toàn vẹn RAM. Tigress không phải mã nguồn mở miễn phí cho mọi mục đích; chỉ nghiên cứu theo điều khoản cho phép | Chưa chọn triển khai |
| REF-06 | Windowed Decryption | Tài liệu Sentinel V3 | Chưa tìm được hệ thống mở tương đương đã kiểm chứng | Chưa có ứng viên đạt |
| REF-07 | Function Protection | LLVM, tài liệu Sentinel Envelope Plus | Nền tảng nghiên cứu, không mặc định chuyển được native ARX đã build sang IR | Chưa chọn triển khai |
| REF-08 | Anti-Tamper chuyên sâu | Tài liệu Sentinel, nghiên cứu mở | Chưa tìm được bộ mã nguồn mở hoàn chỉnh đáp ứng mục tiêu | Chưa có ứng viên đạt |
| REF-09 | License Enforcement | [Licensecc](https://github.com/open-license-manager/licensecc), TidiDcad V55 | Đã có nền tảng cấp phép; không thay hệ thống hiện hành | Giữ nguyên, nghiệm thu hồi quy |
| REF-10 | Cưỡng chế xác minh mã | [Microsoft App Control](https://learn.microsoft.com/en-us/windows/security/application-security/application-control/app-control-for-business/appcontrol-and-applocker-overview), chính sách nạp CAD | Năng lực nền tảng Windows, không phải mã nguồn mở; không mặc định yêu cầu khách đổi chính sách máy | Chờ đánh giá tương thích |

Các mã REF chỉ dùng theo dõi nguồn nghiên cứu, không thay ID năng lực SEC hoặc ca nghiệm thu AT01–AT08. Đây là danh sách ứng viên, không phải danh sách thư viện bắt buộc hay chứng nhận tương đương Sentinel.

**Sàng lọc giấy phép:** LIEF (Apache-2.0), OpenSSL 3.x (Apache-2.0), LLVM (Apache-2.0 WITH LLVM-exception), osslsigncode (GPL-3.0 theo dự án), fsverity-utils (MIT; phân biệt với mã Linux kernel). Phải đọc LICENSE/NOTICE của đúng phiên bản/commit và dependency trước khi sao chép, liên kết hoặc phân phối; đánh giá nghĩa vụ GPL riêng, không mặc định được nhúng vào sản phẩm đóng. Công cụ có thể chỉ dùng để tham khảo hoặc kiểm chứng. Không tự thêm dependency khi thành phần hiện hành đủ dùng.

##### Quy trình bắt buộc theo giai đoạn

| Bước | Công việc | Điều kiện chuyển bước |
|---|---|---|
| 01 | Đọc tài liệu chính thức Sentinel Envelope và giới hạn từng engine | Có nguồn, phiên bản, năng lực xác nhận được; phân biệt thông tin công khai và giả thuyết |
| 02 | Phân rã mục tiêu thành năng lực và tiêu chí nghiệm thu | Mỗi năng lực có mục đích, ranh giới bảo mật, đối tượng và hành vi mong đợi |
| 03 | Tìm ứng viên mở/tiêu chuẩn/API tương ứng | Có URL nguồn chính thức và ma trận đối chiếu năng lực |
| 04 | Rà chất lượng, phiên bản, giấy phép, phụ thuộc | Ghi commit/tag, LICENSE/NOTICE, điều kiện dùng thương mại, hỗ trợ Windows x64, rủi ro và bảo trì |
| 05 | Build/chạy thử nguyên bản | Workspace cô lập; log và chứng cứ thật, không tự sửa upstream để ép PASS |
| 06 | Đánh giá từng ứng viên | Đúng chức năng, khả năng tích hợp native, hiệu năng, giới hạn bảo mật và tình huống lỗi |
| 07 | Chọn đúng thành phần cần thiết | Có lý do chọn/loại, ưu tiên đơn giản và tận dụng V55; không ghép tất cả thư viện |
| 08 | Thiết kế DcadEnvelope/SEC-AT | Chốt trust anchor, đối tượng bảo vệ, ranh giới cưỡng chế, fail-closed, tương thích build/CAD; đánh giá tác động và được chủ dự án duyệt trước code |
| 09 | Triển khai và kiểm thử độc lập | Tuân thủ STD-18 AI-14–AI-18, kiểm tra diff, test lại nguồn cuối |
| 10 | Tích hợp thử DJoin native AutoCAD 2022 x64 | Đúng baseline được xác nhận; Build/APPLOAD/Runtime và kiểm thử chức năng giữ nguyên riêng |
| 11 | Đối chiếu với chuẩn Sentinel | Báo đạt/một phần/chưa đạt theo tiêu chí có chứng cứ; ghi giới hạn thực tế, không tự tuyên bố tương đương |
| 12 | Nghiệm thu và cập nhật tiến độ | Chủ dự án xác nhận; cập nhật trực tiếp mục này trong README DCAD theo STD-17, không tạo file roadmap riêng |

**Nguyên tắc thực hiện:** kế thừa nguồn tốt đã được kiểm chứng; triển khai theo đặc tả và API chuẩn; không tự sáng tạo thuật toán mật mã; không coi mã hóa, ký số hay biến đổi mã đơn lẻ là hệ thống Anti-Tamper hoàn chỉnh. Nếu không tìm được ứng viên đủ tốt hoặc không thể xác minh baseline/giấy phép, ghi rõ blocker và tiếp tục nghiên cứu trước khi triển khai. Các giai đoạn bảo vệ file, bảo vệ điểm kiểm tra bản quyền, bảo vệ mã và bộ nhớ phải có tiêu chí riêng. Không được tự ý làm lại Gate, cấp License, thay chính sách Windows/CAD hoặc mở rộng ngoài phạm vi.

**Tiến độ hiện tại:** phương pháp nghiên cứu đã được duyệt; danh sách ứng viên sơ bộ đã lập. Chưa khóa phiên bản upstream, chưa build/test nguyên bản, chưa xác nhận giấy phép theo commit, chưa chọn dependency cuối cùng, chưa thiết kế chi tiết hoặc code SEC-AT. Ưu tiên tiếp theo: khảo sát SEC-AT theo bước 01–04, sau đó build/test ứng viên cần thiết. Tất cả cổng chưa có bằng chứng giữ NotVerified.

#### 4. Tài liệu chuẩn tham chiếu

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

#### 5. Lịch sử tiến độ

- 26/11/2026: V55 được chủ dự án xác nhận chạy OK; roadmap lấy Sentinel LDK làm chuẩn; chọn chống sửa Add-in làm giai đoạn tiếp theo. Chưa code giai đoạn SEC-AT. Giữ nguyên snapshot V55 và các quy ước đang hiệu lực.
- 26/11/2026: Chủ dự án duyệt phương pháp nghiên cứu SEC-AT: Sentinel Envelope là chuẩn tham chiếu, các thành phần mở/tiêu chuẩn là cơ sở phát triển độc lập; thêm ma trận REF-01–REF-10 và quy trình 12 bước ngay trong README. Chưa chọn dependency cuối, chưa code, chưa tăng version.
