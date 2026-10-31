# DCAD — Hệ thống quản lý Add-in CAD

**DCAD là repository tổng hợp trạng thái** của các Add-in; mỗi Add-in có repository riêng để lưu ZIP mã nguồn, DLL, changelog và lịch sử phiên bản. Không chép ZIP, SDK hoặc DLL của Add-in vào repository DCAD.

## Danh mục Add-in

| Add-in | Phiên bản mới nhất hiện có trên GitHub | Repository | ZIP | Trạng thái |
| --- | --- | --- | --- | --- |
| DBox | V5 | [Tidi6969/DBox](https://github.com/Tidi6969/DBox) | [DBox-V5.zip](https://github.com/Tidi6969/DBox/blob/main/V5/DBox-V5.zip) | Đã lưu ZIP V5; build và chạy thử trên CAD: chưa được xác minh ở danh mục này |
| DPunch | V390 | [Tidi6969/Dpunch](https://github.com/Tidi6969/Dpunch) | [DPunch-V390.zip](https://github.com/Tidi6969/Dpunch/blob/main/V390/DPunch-V390.zip) | Đã lưu ZIP V390; build và chạy thử trên CAD: chưa được xác minh ở danh mục này |
| DJoin | V14 (nguồn tham khảo cũ) | Chưa xác nhận repository | — | Chưa xác minh có bản lưu trên GitHub |

**Đối chiếu kho ngày 31/10/2026:** đã kiểm tra sự tồn tại của các đường dẫn ZIP nêu trong bảng qua cây file GitHub. Việc một file ZIP tồn tại **không** chứng minh build thành công hay NETLOAD/runtime đã PASS.

## Mục tiêu CAD

Các target tiêu chuẩn của hệ thống là **AutoCAD 2022, AutoCAD 2025 và GstarCAD 2027**, nhưng phạm vi build/kiểm thử của từng phiên bản phải dựa trên log và chứng cứ riêng; không suy từ danh sách target tiêu chuẩn.

## Quy trình giao việc và tự đồng bộ

1. Chủ dự án giao yêu cầu sửa code hoặc phiên bản mới **tại ChatGPT** và chỉ định baseline, phiên bản đích, CAD mục tiêu (hoặc dùng các thông tin đã thống nhất trong cuộc hội thoại).
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

## Chủ sở hữu

GitHub: [Tidi6969](https://github.com/Tidi6969)
