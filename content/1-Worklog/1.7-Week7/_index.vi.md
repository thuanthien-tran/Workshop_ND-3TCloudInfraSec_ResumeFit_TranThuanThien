---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---


### Mục tiêu tuần 7:

* Cấu hình các loại bản ghi DNS và chính sách định tuyến của Amazon Route 53.
* Thiết lập CDN Amazon CloudFront để tối ưu hóa tốc độ tải trang.
* Cấu hình bảo mật HTTPS sử dụng chứng chỉ số miễn phí từ AWS Certificate Manager (ACM).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Tìm hiểu dịch vụ DNS Amazon Route 53. Nghiên cứu các chính sách định tuyến (Routing Policies): Simple, Weighted, Geolocation, Failover. | 03/06/2026 | 03/06/2026 | [Amazon Route 53 Routing Policies Guide](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html) |
| 5 | - Tìm hiểu mạng lưới CDN Amazon CloudFront, cơ chế cache ở Edge Locations và tính năng Origin Access Control (OAC). | 04/06/2026 | 04/06/2026 | [CloudFront Developer Guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html) |
| 6 | - Thực hành cấu hình CloudFront Distribution lấy nguồn từ S3 bucket riêng tư. Sử dụng OAC để giới hạn người dùng truy cập trực tiếp qua S3. | 05/06/2026 | 05/06/2026 | [S3 Origin Access Control (OAC) CloudFront Integration](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/DownloadDistS3AndCustomOrigins.html) |
| 2 | - Tìm hiểu AWS Certificate Manager (ACM) để tạo chứng chỉ SSL/TLS miễn phí, thực hiện xác thực qua bản ghi DNS. | 08/06/2026 | 08/06/2026 | [AWS ACM Overview Guide](https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html) |
| 3 | - Tích hợp tên miền riêng vào Route 53 bằng Alias record trỏ về CloudFront Distribution. Gắn chứng chỉ ACM SSL/TLS cho CloudFront để chạy HTTPS. | 09/06/2026 | 09/06/2026 | [CloudFront Custom Domain Mapping Guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-custom-filenames.html) |


### Kết quả đạt được tuần 7:

* Hiểu cơ chế giảm độ trễ truy cập web toàn cầu bằng cách cache nội dung tại các Edge Locations.
* Bảo mật kênh truyền dữ liệu người dùng cuối sử dụng giao thức mã hóa SSL/TLS (HTTPS).
* Quản lý định tuyến và ánh xạ tên miền tùy chỉnh sử dụng Route 53.
