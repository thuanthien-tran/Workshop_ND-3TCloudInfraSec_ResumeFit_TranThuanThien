---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---


### Mục tiêu tuần 4:

* Triển khai và quản lý các ổ lưu trữ Amazon EBS và cơ chế Snapshots.
* Khởi tạo và kết nối tới một cơ sở dữ liệu Amazon Relational Database Service (RDS).
* Giám sát tài nguyên hệ thống và thiết lập cảnh báo tự động thông qua Amazon CloudWatch.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Tìm hiểu kiến trúc Amazon EBS. Thực hành tạo EBS volume và gắn (attach) vào EC2 instance đang chạy. | 13/05/2026 | 13/05/2026 | [Amazon EBS Volume Types Guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) |
| 5 | - Thực hiện định dạng và mount ổ đĩa EBS trên Linux. Tìm hiểu cách tạo EBS snapshot và khôi phục ổ đĩa từ snapshot. | 14/05/2026 | 14/05/2026 | [EBS Volume Management Guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html) |
| 6 | - Tìm hiểu dịch vụ cơ sở dữ liệu Amazon RDS. Hiểu về các loại database engines, cấu hình dung lượng, Multi-AZ và Read Replicas. | 15/05/2026 | 15/05/2026 | [AWS RDS Introduction Guide](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html) |
| 2 | - Triển khai database instance MySQL/PostgreSQL trên RDS. Cấu hình Security Group để cho phép kết nối an toàn từ EC2 web server. | 18/05/2026 | 18/05/2026 | [Amazon RDS Getting Started Guide](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_GettingStarted.html) |
| 3 | - Tìm hiểu Amazon CloudWatch. Cấu hình giám sát tài nguyên (CPU, Disk, Memory) và thiết lập Alarms gửi cảnh báo qua Amazon SNS. | 19/05/2026 | 19/05/2026 | [Amazon CloudWatch Getting Started Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/GettingStarted.html) |


### Kết quả đạt được tuần 4:

* Cấu hình thành công ổ đĩa ngoài lưu trữ dữ liệu bền vững (persistent storage) cho EC2 bằng EBS.
* Triển khai cơ sở dữ liệu quan hệ RDS ổn định và thiết lập kết nối bảo mật với EC2.
* Thiết lập hệ thống giám sát và gửi mail cảnh báo thời gian thực tự động khi quá tải tài nguyên.
