---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---


### Mục tiêu tuần 2:

* Nắm vững kiến thức IAM cơ bản: Users, Groups, Policies và Roles.
* Triển khai và truy cập các thực thể Amazon EC2 thông qua kết nối SSH.
* Cấu hình lưu trữ Amazon S3 bucket và quản lý các đối tượng.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Tìm hiểu AWS Identity and Access Management (IAM). Thực hành tạo IAM Users, User Groups, Policies (cấu trúc JSON) và IAM Roles. | 29/04/2026 | 29/04/2026 | [AWS IAM User Guide Introduction](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html) |
| 5 | - Tìm hiểu các khái niệm Amazon EC2: instance types, AMI (Amazon Machine Image), Security Groups và Key Pairs. | 30/04/2026 | 30/04/2026 | [AWS EC2 Concepts](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html) |
| 6 | - Thực hành khởi tạo EC2 instance chạy Linux. Cấu hình inbound rules cho Security Group. Kết nối SSH vào instance từ máy local. | 01/05/2026 | 01/05/2026 | [Connecting to Linux Instance Guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstances.html) |
| 2 | - Tìm hiểu dịch vụ Amazon S3: các storage classes (Standard, IA, Glacier), bucket policies và Lifecycle Rules. | 04/05/2026 | 04/05/2026 | [AWS S3 Intro Guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html) |
| 3 | - Thực hành tải lên và quản lý tệp trên Amazon S3: Tạo bucket, upload files, cấu hình public access và test đường dẫn URL của object. | 05/05/2026 | 05/05/2026 | [Amazon S3 Getting Started](https://docs.aws.amazon.com/AmazonS3/latest/userguide/GetStartedWithS3.html) |


### Kết quả đạt được tuần 2:

* Tạo thành công IAM admin user thay thế root account theo khuyến nghị bảo mật.
* Khởi tạo và kết nối thành công máy chủ ảo Linux EC2 qua giao thức SSH.
* Hiểu cách quản lý lưu trữ S3, phân quyền bucket và tối ưu chi phí với Lifecycle Policies.
