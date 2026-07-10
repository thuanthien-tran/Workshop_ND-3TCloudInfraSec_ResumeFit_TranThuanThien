---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---


### Mục tiêu tuần 8:

* Nắm vững các nguyên tắc thiết kế hạ tầng dưới dạng mã (Infrastructure as Code - IaC).
* Lập trình viết các tệp mẫu CloudFormation có tính tái sử dụng bằng YAML/JSON.
* Khởi tạo, cập nhật và dọn dẹp các CloudFormation stacks qua giao diện Console và CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Tìm hiểu khái niệm Infrastructure as Code (IaC) và cách AWS CloudFormation đơn giản hóa việc quản trị tài nguyên. | 10/06/2026 | 10/06/2026 | [AWS CloudFormation Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html) |
| 5 | - Nghiên cứu cú pháp viết template CloudFormation sử dụng YAML/JSON: Parameters, Resources, Properties và Outputs. | 11/06/2026 | 11/06/2026 | [CloudFormation Template Sections Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html) |
| 6 | - Thực hành viết một template đơn giản để khởi tạo cấu hình một máy chủ ảo EC2 và một Security Group liên kết. | 12/06/2026 | 12/06/2026 | [CloudFormation Template Basics](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-guide.html) |
| 2 | - Tiến hành deploy template lên CloudFormation để tạo Stack. Theo dõi nhật ký sự kiện tạo tài nguyên và hiểu cơ chế rollback khi có lỗi. | 15/06/2026 | 15/06/2026 | [AWS CloudFormation Stacks Concepts](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacks.html) |
| 3 | - Thực hành cập nhật thay đổi tài nguyên bằng cách cập nhật Stack. Tiến hành xóa Stack để tự động dọn dẹp các tài nguyên nhằm tránh mất phí. | 16/06/2026 | 16/06/2026 | [AWS Stack Update Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) |


### Kết quả đạt được tuần 8:

* Loại bỏ thao tác click thủ công truyền thống bằng việc quản trị hạ tầng qua file mã nguồn cấu hình.
* Hiểu sâu các trạng thái triển khai Stack, nhật ký logs và cơ chế tự động khôi phục (rollback) khi gặp sự cố.
* Viết tài liệu Blueprint triển khai hệ thống định dạng YAML có khả năng quản lý phiên bản qua Git.
