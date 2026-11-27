# 3D Packaging Mockup

Ứng dụng trình duyệt dựng bản trải carton 2D và mockup thùng carton 3D, chạy trực tiếp từ một trang HTML; không cần bước build.

## Chức năng chính

- Tạo bản trải 2D theo kích thước dài, rộng, cao, độ dày carton, cánh gập, khe xẻ và mối nối.
- Chiều cao cánh mặc định tự theo W/2 khi đổi chiều rộng (có thể tắt tự động và nhập tay). Chồng mí cánh chính được tính theo tổng L1 + L2 so với W: ví dụ 210 + 210 mm trên W=400 mm cho 20 mm chồng mí thật. Người dùng có thể nhập mức bù tự do, không bị giới hạn 5 mm; phần bù chỉ điều chỉnh mô hình khi tick xác nhận đóng khít.
- Có thể bật riêng chế độ nhập chiều cao cho từng trong bốn cánh trên và từng trong bốn cánh dưới. Các chiều cao riêng điều khiển mô hình 3D; bản trải 2D hiện tiếp tục dùng chiều cao cánh chung.
- Chèn artwork PNG/JPG/WebP, di chuyển, co giãn, gôm tẩy và thêm ghi chú; hỗ trợ Undo/Redo.
- Lưu/mở dự án JSON gồm kích thước, vật liệu, tùy chọn 3D, tám chiều cao cánh riêng, artwork, chữ/ghi chú và trạng thái khung nhìn 2D; dự án JSON cũ không có chiều cao riêng vẫn mở được.
- Dựng thùng carton 3D với vật liệu giấy, lớp sóng, màu sắc, băng keo và góc mở cánh; khi đóng, đường ráp giữa hai cánh luôn hiển thị, còn phần chồng mí thật được tô vùng màu và đánh dấu hai mép.
- Xem các góc camera, phát/tua hoạt ảnh trình tự gập cánh và xuất ảnh PNG.
- Xuất mô hình 3D định dạng GLB để dùng trong công cụ tương thích glTF.
- Xuất bản trải 2D thành ảnh PNG độ phân giải cao hoặc SVG vector.

## Sử dụng

Mở `index.html` bằng trình duyệt có hỗ trợ JavaScript modules và WebGL. Ứng dụng tải Three.js từ jsDelivr nên cần kết nối Internet. Nhập kích thước và chọn **DỰNG BẢN TRẢI PHẲNG 2D NGAY!** để kiểm tra bản trải; chọn **DỰNG MOCKUP 3D NGAY** để xem thùng. Trong chế độ 3D, dùng thanh công cụ để đổi góc nhìn, xuất PNG hoặc **Xuất 3D GLB**.

Artwork hiện nhận PNG, JPG và WebP. Tệp PDF chưa được rasterize trực tiếp trong ứng dụng; cần chuyển trang thiết kế thành ảnh trước khi tải lên. Tệp dự án JSON nhúng dữ liệu artwork nên có thể lớn; artwork nhúng tối đa 45 MB và toàn bộ tệp dự án tối đa 50 MB (áp dụng khi lưu và mở).

## Chạy máy chủ cục bộ

```bash
python3 -m http.server 8000
```

Sau đó mở `http://localhost:8000`.
