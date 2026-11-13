# 3D Packaging Mockup Studio V0.1

## Chạy thử
- Mở `index.html` bằng trình duyệt có kết nối Internet; Three.js và OrbitControls được tải từ jsDelivr.
- Để đưa lên GitHub Pages: tạo repository, tải `index.html` lên thư mục gốc, vào Settings → Pages → Deploy from a branch → chọn `main` và `/ (root)`.

## Chức năng hiện có
- Dựng mô hình thùng carton nắp đối kiểu RSC / FEFCO 0201 ở mức thử nghiệm.
- Nhập dài, rộng, cao, lưỡi gà và độ dày carton.
- Xoay, zoom, chọn góc nhìn trước/trên/hông.
- Điều khiển mở/đóng cánh trên và dưới.
- Tải PNG/JPG artwork để xem trước; chế độ kraft và màu kỹ thuật.
- Xuất ảnh PNG khung nhìn hiện tại.

## Giới hạn V0.1 cần kiểm tra
- Artwork mapping theo toàn bộ dieline chưa hoàn thiện; bản hiện tại là nền tảng dựng hình và điều khiển hình học, chưa tự phân tích file AI/CDR/PDF.
- Chưa mô phỏng chính xác tai dán, khe hở cánh, bù trừ độ dày, đường bế/cấn, mép sóng và quy trình gấp thực tế.
- Dữ liệu ảnh artwork cần bản trải cắt sát, theo quy ước bố cục được thống nhất ở phiên bản tiếp theo.
- Cần kiểm tra lại hướng mở từng cánh và quy ước kích thước theo mẫu sản xuất thực tế.

## Kế hoạch V0.2
- Thêm bộ nhập dieline SVG/PDF.
- Ánh xạ vùng artwork riêng cho từng mặt và từng cánh.
- Thêm cấu hình khoảng hở cánh, tai dán và độ dày vật liệu.
- Lưu/tải cấu hình dự án JSON.
