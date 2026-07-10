---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---


### Mục tiêu tuần 10:

* Đóng gói ứng dụng web vào container sử dụng công nghệ Docker.
* Quản lý lưu trữ và chia sẻ Docker image thông qua Amazon ECR.
* Hiểu kiến trúc điều phối container chạy Serverless bằng Amazon ECS và AWS Fargate.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Tìm hiểu nền tảng Docker, viết Dockerfile để đóng gói (containerize) ứng dụng web mẫu Node.js/Python. | 24/06/2026 | 24/06/2026 | [Getting Started with Docker Guide](https://docs.docker.com/get-started/) |
| 5 | - Thực hành build Docker images từ Dockerfile. Chạy và kiểm tra hoạt động của container trực tiếp ở môi trường local. | 25/06/2026 | 25/06/2026 | [Docker CLI Build Guide](https://docs.docker.com/engine/reference/commandline/build/) |
| 6 | - Nghiên cứu Amazon Elastic Container Registry (ECR). Tạo repository trên ECR, đăng nhập bằng AWS CLI và push Docker image lên. | 26/06/2026 | 26/06/2026 | [Amazon ECR Guide](https://docs.aws.amazon.com/AmazonECR/latest/userguide/ECR_GetStarted.html) |
| 6 | - Tìm hiểu kiến trúc Amazon ECS: Clusters, Task Definitions, Services. So sánh EC2 launch type và Serverless Fargate launch type. | 26/06/2026 | 26/06/2026 | [Amazon ECS Getting Started Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/getting-started.html) |


### Kết quả đạt được tuần 10:

* Đóng gói ứng dụng thành công tạo ra các file deploy độc lập, chạy mọi nơi không phụ thuộc hệ điều hành với Docker.
* Quản lý lưu trữ Docker images bảo mật trên Cloud bằng dịch vụ ECR.
* Nắm bắt được kiến trúc và nguyên lý điều phối, vận hành container không cần quản lý máy chủ với ECS và Fargate.
