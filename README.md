# Chi Đoàn Thanh Niên — Ultra 2026

Website tĩnh giới thiệu tin tức và hoạt động Chi đoàn, xây dựng bằng HTML, CSS và JavaScript thuần. Không cần cài đặt framework hoặc chạy máy chủ riêng.

## Tính năng

- Giao diện tiếng Việt, tương thích máy tính, máy tính bảng và điện thoại.
- Danh sách tin hoạt động được dựng tự động từ dữ liệu JavaScript.
- 18 bài viết mẫu: 8 bài có sẵn và 10 bài bổ sung từ **24/11/2026 đến 31/12/2026**.
- Tìm kiếm theo tiêu đề, nội dung và ngày.
- Lọc nhóm bài viết cũ/mới; sắp xếp theo ngày hoặc tiêu đề.
- Lưu bài yêu thích trên trình duyệt bằng `localStorage`.
- Chế độ sáng/tối, chia sẻ bài viết, in trang và xuất dữ liệu JSON.
- Hỗ trợ `prefers-reduced-motion` và kiểu in.

> Lưu ý: nội dung bài viết là dữ liệu mẫu để biên tập. Hãy xác minh ngày, hoạt động và thông tin thực tế trước khi công bố.

## Cấu trúc dự án

```text
.
├── index.html
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml
```

## Chạy thử

Mở trực tiếp `index.html` bằng trình duyệt. Website không yêu cầu bước build.

## Triển khai lên GitHub Pages

1. Tạo repository trên GitHub.
2. Đưa `index.html`, `README.md` và thư mục `.github/workflows/` lên nhánh `main`.
3. Mở **Settings → Pages**.
4. Trong **Build and deployment → Source**, chọn **GitHub Actions**.
5. Push commit lên nhánh `main` (hoặc chạy workflow thủ công ở tab **Actions**).
6. Sau khi workflow hoàn tất, mở địa chỉ GitHub Pages hiển thị trong **Settings → Pages**.

Workflow nằm tại `.github/workflows/deploy.yml`. GitHub Actions sẽ tải lên nội dung website tĩnh và triển khai lên GitHub Pages.

## Cập nhật nội dung

Trong `index.html`, tìm mảng `posts` trong thẻ `<script>`. Mỗi bài viết có dạng:

```js
{
  title: "Tiêu đề hoạt động",
  date: "24/11/2026",
  content: "Nội dung giới thiệu hoạt động."
}
```

Ngày dùng định dạng `DD/MM/YYYY`. Khi thêm bài viết, nên giữ nội dung ngắn gọn, chính xác và kiểm tra lại ngày tháng.

## Lưu ý kỹ thuật

- Dữ liệu yêu thích được lưu cục bộ trên từng trình duyệt; hiện chưa có đăng nhập hoặc đồng bộ giữa nhiều thiết bị.
- Chức năng xuất JSON tạo bản sao dữ liệu bài viết hiện có.
- Chức năng chia sẻ dùng Web Share API nếu trình duyệt hỗ trợ; nếu không, trình duyệt có thể dùng thao tác sao chép khi Clipboard API khả dụng.
- Đây là website tĩnh, chưa có trang quản trị hoặc cơ sở dữ liệu phía máy chủ.

## Giấy phép

Chưa chỉ định giấy phép. Hãy bổ sung tệp `LICENSE` nếu muốn công bố quyền sử dụng và phân phối mã nguồn.
