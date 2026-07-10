---
title: "5.5.2 Khởi tạo SQS Queues"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.5.2. Khởi tạo SQS Queues

1. Chuyển đến giao diện **SQS**. Tạo một hàng đợi Standard có tên `ResumeMatching-DLQ` (Dead Letter Queue) dùng để hứng các message bị lỗi trong quá trình xử lý.
   ![Tạo DLQ Queue](/images/5-Workshop/Tao_queue.jpg)

2. Khởi tạo hàng đợi chính mang tên `ResumeMatching-Queue`.
   ![Tạo Main Queue](/images/5-Workshop/Tao_main_queue.jpg)
