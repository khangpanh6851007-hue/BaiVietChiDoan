# Chi đoàn Thanh niên — Youth Connect Ultra 2026

Website tĩnh giới thiệu tin tức, hoạt động và công cụ điều hành Chi đoàn Thanh niên.

## Tính năng

- Trang tin hoạt động Chi đoàn với 18 bài viết mẫu trong năm 2026.
- Tìm kiếm bài viết, lọc theo thời gian và sắp xếp.
- Lưu bài viết yêu thích trên trình duyệt.
- Chia sẻ bài viết, in trang và xuất dữ liệu JSON.
- Chế độ sáng/tối.
- Tạo hoạt động, gửi sáng kiến, đăng ký tình nguyện và soạn thông báo.
- Lưu dữ liệu nội bộ bằng `localStorage` trên thiết bị/trình duyệt hiện tại.
- Giao diện responsive cho điện thoại và máy tính.

## Cấu trúc thư mục

```text
.
├── index.html
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml
```

> Đổi tên file HTML hiện có (`index-ultra(1).html`) thành `index.html` và đặt ở thư mục gốc repository. GitHub Pages mặc định tìm trang chủ tại `index.html`.

## Chạy thử trên máy

Mở trực tiếp `index.html` bằng trình duyệt. Không cần cài đặt package hoặc máy chủ backend.

## Triển khai GitHub Pages

1. Tạo repository trên GitHub.
2. Đưa `index.html`, `README.md` và thư mục `.github/workflows/` vào nhánh `main`.
3. Mở **Settings → Pages** của repository.
4. Trong **Build and deployment**, chọn **GitHub Actions** làm source.
5. Push commit lên nhánh `main`. Workflow `Deploy GitHub Pages` sẽ tự động triển khai website.
6. Sau khi workflow hoàn tất, mở URL GitHub Pages hiển thị trong phần **Settings → Pages**.

## Lưu ý về dữ liệu

Website hiện là ứng dụng frontend tĩnh. Hoạt động, sáng kiến, đăng ký và bài viết đã lưu được lưu trong `localStorage` của trình duyệt đang sử dụng; dữ liệu không tự đồng bộ giữa các thiết bị hoặc người dùng. Muốn dùng chung dữ liệu, đăng nhập, phân quyền hoặc điểm danh QR thực tế, cần bổ sung backend và cơ sở dữ liệu.

## Công nghệ

- HTML5
- CSS3
- JavaScript thuần
- GitHub Actions
- GitHub Pages
