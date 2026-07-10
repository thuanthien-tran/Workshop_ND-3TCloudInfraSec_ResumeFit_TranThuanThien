---
title: "Worklog Tuần 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---


### Mục tiêu tuần 3:

* Hiểu nền tảng về mạng ảo trong AWS.
* Tạo một Virtual Private Cloud (VPC) tùy chỉnh với Public và Private subnets.
* Cấu hình Internet Gateways, NAT Gateways và Route Tables.
* Thiết lập bảo mật mạng sử dụng Security Groups và Network ACLs (NACLs).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Tìm hiểu kiến trúc AWS VPC, cách chia subnet và cấp phát địa chỉ IP CIDR blocks. | 06/05/2026 | 06/05/2026 | [How Amazon VPC Works](https://docs.aws.amazon.com/vpc/latest/userguide/how-it-works.html) |
| 5 | - Thực hành tạo VPC tùy chỉnh. Cấu hình Public và Private Subnet trên các Availability Zone khác nhau để tăng tính sẵn sàng. | 07/05/2026 | 07/05/2026 | [VPC & Subnets Guide](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) |
| 6 | - Cấu hình Internet Gateway (IGW) cho luồng mạng công cộng và NAT Gateway cho phép Private Subnet truy cập internet một chiều. | 08/05/2026 | 08/05/2026 | [NAT Gateway Setup Docs](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html) |
| 2 | - Thiết lập Route Tables cho Public và Private Subnets. Ánh xạ các route thích hợp qua IGW hoặc NAT Gateway. | 11/05/2026 | 11/05/2026 | [Route Tables Guide](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html) |
| 3 | - Nghiên cứu và cấu hình Security Group (Stateful) và Network ACL (Stateless). Kiểm tra kết nối mạng (ping/curl) giữa các tài nguyên để xác thực. | 12/05/2026 | 12/05/2026 | [Security Groups in VPC Guide](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) |


### Kết quả đạt được tuần 3:

* Thiết kế và triển khai thành công hạ tầng mạng ảo tùy chỉnh (VPC) trên AWS.
* Có kinh nghiệm cô lập cơ sở dữ liệu trong private subnet trong khi vẫn chạy web server ở public subnet.
* Cấu hình và kiểm soát truy cập mạng ở cả cấp độ EC2 instance (Security Groups) và cấp độ Subnet (NACLs).
