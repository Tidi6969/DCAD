# DCAD — AutoCAD Add-in Development System

DCAD là hệ thống quản lý các dự án Add-in AutoCAD độc lập.

## Nguyên tắc tổ chức

- **DCAD (repository này):** danh mục dự án, tài liệu chung, quy trình phát triển và liên kết phát hành.
- **Mỗi Add-in có repository riêng:** mã nguồn, lịch sử thay đổi, phiên bản và bản phát hành độc lập.
- Không đưa mã nguồn hoặc DLL của các Add-in vào repository DCAD tổng thể.

## Danh mục Add-in dự kiến

| Add-in | Phiên bản nguồn tham khảo | Repository | Trạng thái |
| --- | --- | --- | --- |
| DBox | V4 | [Tidi6969/DBox](https://github.com/Tidi6969/DBox) | Đã tạo repository; đang nhập mã nguồn |
| DJoin | V14 | DCAD-DJoin | Chưa thiết lập |
| DPunch | V390 | DCAD-DPunch | Chưa thiết lập |

Các phiên bản trên là tên gói nguồn tham khảo, **không phải** bản phát hành đã được xác nhận trên GitHub. Chỉ thêm liên kết repository khi repository đó thực sự được tạo.

## Quy trình phát triển dự kiến

1. Mô tả yêu cầu thay đổi cho một Add-in cụ thể.
2. Chỉnh sửa và lưu mã nguồn trong repository của Add-in đó.
3. Kiểm tra thay đổi, tạo commit và ghi nhận phiên bản.
4. Build bằng môi trường Windows phù hợp với .NET và AutoCAD tương ứng.
5. Sau khi build và kiểm tra thành công, đưa gói chạy được lên GitHub Releases.
6. Cập nhật đường dẫn phiên bản tại danh mục DCAD.

> Lưu ý: Việc tự động build DLL, tạo Release và kết nối Codex cần được cấu hình riêng cho từng dự án. Chưa coi các bước đó là đã hoạt động.

## Quy ước gợi ý

- Repository quản lý: `Tidi6969/DCAD`
- Repository Add-in: `Tidi6969/<TênAddin>` (ví dụ: `Tidi6969/DBox`)
- Mỗi Add-in có `README.md`, hướng dẫn build và changelog riêng.
- Không commit file tạm của Visual Studio như `.vs/`, `bin/`, `obj/` trừ khi có lý do kỹ thuật cụ thể.

## Chủ sở hữu

GitHub: [Tidi6969](https://github.com/Tidi6969)
