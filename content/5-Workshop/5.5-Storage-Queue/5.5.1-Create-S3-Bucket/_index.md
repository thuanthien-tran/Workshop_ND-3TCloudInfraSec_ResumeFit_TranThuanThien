---
title: "5.5.1 S3 Bucket Initialization"
date: 2024-01-01
weight: 1
chapter: false
---

### 5.5.1. S3 Bucket Initialization

1. In the **S3** Console, click **Create bucket** to provision storage space for candidate CVs and JD requirements.
   ![Create S3 Bucket](/images/5-Workshop/Tao_S3.jpg)

2. Create a folder directory inside your S3 bucket.
   ![Create Folder in S3](/images/5-Workshop/Create_Folder_S3.jpg)

3. In the **Permissions** tab, edit the **Cross-origin resource sharing (CORS)** rule. Add JSON configurations authorizing `GET`, `PUT`, and `POST` methods to enable direct client uploads.
   ![Configure S3 CORS](/images/5-Workshop/Bo_sung_CORS_S3.jpg)
