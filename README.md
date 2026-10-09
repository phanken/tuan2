# Chấm công PWA - lưu cục bộ và tự cập nhật

- Tải toàn bộ nội dung thư mục `chamcong_web` lên GitHub Pages, bao gồm `version.json`.
- PWA kiểm tra phiên bản lúc mở, khi quay lại ứng dụng, khi có mạng và mỗi 60 giây lúc đang mở.
- Khi có bản mới, PWA tự tải lại một lần; không cần gỡ ứng dụng.
- Dữ liệu `chamcong_data` tiếp tục lưu trong localStorage trên từng thiết bị, không bị xóa bởi cơ chế cập nhật.
- Mỗi lần phát hành sau, thay đổi phiên bản ở `version.json` và `window.CHAMCONG_BUILD_VERSION` trong `index.html`, đồng thời thay đổi tên CACHE trong `sw.js` để cập nhật tài nguyên offline.
- iOS có thể trì hoãn cập nhật do cache hoặc chính sách chạy nền; cần mở PWA khi có mạng.
- Sao lưu JSON định kỳ vì xóa dữ liệu Safari/PWA có thể làm mất dữ liệu.
