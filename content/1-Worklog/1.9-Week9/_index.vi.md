---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---


### Mục tiêu tuần 9:

* Bảo vệ ứng dụng web khỏi các lỗ hổng bảo mật phổ biến bằng cách sử dụng AWS WAF.
* Hiểu các cơ chế chống tấn công từ chối dịch vụ DDoS qua AWS Shield.
* Lưu trữ và quản trị thông tin mật bằng AWS Secrets Manager và Systems Manager Parameter Store.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Tìm hiểu các mối đe dọa an ninh mạng (SQLi, XSS) và cách AWS WAF lọc lưu lượng truy cập dựa vào các bộ quy tắc (rules). | 17/06/2026 | 17/06/2026 | [AWS WAF Guide Docs](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html) |
| 5 | - Thực hành khởi tạo Web ACL trên WAF. Cấu hình chặn dải IP độc hại và thiết lập giới hạn tần suất gửi yêu cầu (Rate Limit). | 18/06/2026 | 18/06/2026 | [AWS WAF Web ACLs Guide](https://docs.aws.amazon.com/waf/latest/developerguide/web-acl.html) |
| 6 | - Tìm hiểu cơ chế hoạt động của AWS Shield Standard và Advanced chống lại các cuộc tấn công DDoS ở Layer 3/4 và Layer 7. | 19/06/2026 | 19/06/2026 | [AWS Shield DDoS Info](https://aws.amazon.com/shield/) |
| 2 | - Nghiên cứu AWS Secrets Manager và Systems Manager (SSM) Parameter Store. So sánh tính năng (xoay vòng khóa, chi phí). | 22/06/2026 | 22/06/2026 | [AWS Secrets Manager Guide](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html) |
| 3 | - Thực hành lưu trữ mật khẩu DB ảo trên Secrets Manager. Viết code Python/Node.js để lấy mật khẩu tự động khi chạy thay vì hardcode. | 23/06/2026 | 23/06/2026 | [Retrieving Secrets dynamically with Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/retrieving-secrets.html) |


### Kết quả đạt được tuần 9:

* Bảo vệ thành công ALB hoặc CloudFront Distribution thông qua các quy tắc bảo mật tùy chỉnh trên WAF.
* Hiểu sâu các cơ chế tự động chống tấn công DDoS cho cả hạ tầng và ứng dụng.
* Loại bỏ hoàn toàn việc lưu mật khẩu hoặc khóa kết nối cơ sở dữ liệu dạng văn bản thuần trong mã nguồn.
