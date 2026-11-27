# 3D Packaging Mockup

Ứng dụng trình duyệt dựng bản trải carton 2D và mockup thùng carton 3D, chạy trực tiếp từ một trang HTML; không cần bước build.

## Chức năng chính

- Tạo bản trải 2D theo kích thước dài, rộng, cao, độ dày carton, cánh gập, khe xẻ và mối nối.
- Chèn artwork PNG/JPG/WebP, di chuyển, co giãn, gôm tẩy và thêm ghi chú; hỗ trợ Undo/Redo.
- Dựng thùng carton 3D với vật liệu giấy, lớp sóng, màu sắc, băng keo và góc mở cánh.
- Xem các góc camera, phát/tua hoạt ảnh trình tự gập cánh và xuất ảnh PNG.
- Xuất mô hình 3D định dạng GLB để dùng trong công cụ tương thích glTF.
- Xuất bản trải 2D thành ảnh PNG độ phân giải cao hoặc SVG vector.

## Sử dụng

Mở `index.html` bằng trình duyệt có hỗ trợ JavaScript modules và WebGL. Ứng dụng tải Three.js từ jsDelivr nên cần kết nối Internet. Nhập kích thước và chọn **DỰNG BẢN TRẢI PHẲNG 2D NGAY!** để kiểm tra bản trải; chọn **DỰNG MOCKUP 3D NGAY** để xem thùng. Trong chế độ 3D, dùng thanh công cụ để đổi góc nhìn, xuất PNG hoặc **Xuất 3D GLB**.

Artwork hiện nhận PNG, JPG và WebP. Tệp PDF chưa được rasterize trực tiếp trong ứng dụng; cần chuyển trang thiết kế thành ảnh trước khi tải lên.

## Chạy máy chủ cục bộ

```bash
python3 -m http.server 8000
```

Sau đó mở `http://localhost:8000`.
