---
title: "Blog 3: Data Permissions with AWS Lake Formation"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# A Handy Feature of AWS Lake Formation

Recently, while researching Data Lakes on AWS, I came across an interesting article from AWS about Lake Formation and wanted to share it with everyone.

Looking at the architectural flow:

*   **EMR Spark** reads/writes data directly from S3 using IAM Permissions.
*   **Lake Formation** manages access permissions on data tables in the Glue Catalog.
*   **Athena** queries data using permissions defined in Lake Formation.

This setups leads to a common situation: You can query data using Athena normally, but running Spark to directly access files in S3 triggers an *Access Denied* error. The reason is that Athena and Spark use two different authorization mechanisms:

*   Athena → Lake Formation
*   Spark reading S3 files → IAM / S3 Policy

AWS recently released a feature that addresses this challenge. Lake Formation can now grant temporary credentials so Spark can directly access data in S3 based on permissions configured in Lake Formation, via the API: `GetTemporaryDataLocationCredentials()`.

### Key Benefits of This Feature:

*   Reduces overhead of managing permissions in multiple places.
*   Minimizes *Access Denied* errors caused by mismatched configurations.
*   Simplifies access for Spark, ETL, and Machine Learning workloads.
*   Audits data access activities easily via CloudTrail.

### Important Technical Prerequisites:

*   The S3 Location must be registered with Lake Formation.
*   Requires Amazon EMR 6.15.0+ or 7.1.0+.
*   Apache Iceberg is not yet supported.
*   Cross-Region access is not yet supported.

Overall, this is a highly useful upgrade for AWS Data Lake architectures, especially in environments combining both Athena and EMR Spark.

---

### Solution Architecture Diagram

![AWS Lake Formation Feature](/images/3-BlogsPosted/aws_lake_formation_permissions.png)

---

### Reference Links & Documentation
*   **Original Post on Facebook Group:** [Facebook Post Link](https://www.facebook.com/groups/awsstudygroupfcj/posts/2191055074992786/?notif_id=1782041739635661&notif_t=group_post_approved&ref=notif)
*   **Official AWS Blog Guide:** [AWS Big Data Blog Guide](https://aws.amazon.com/vi/blogs/big-data/access-amazon-s3-data-files-directly-using-aws-lake-formation-permissions/?fbclid=IwY2xjawSu8LtleHRuA2FlbQIxMABicmlkETFDd1poRWJtcTNFMEw4bmJKc3J0YwZhcHBfaWQQMjIyMDM5MTc4ODIwMDg5MgABHlfRqurG5Rir4FRt1bIoRDfriCsPR9wuIOYoTnZdypKxZVcIBVgtWsk4A8C9_aem_pW5Px8mN6tGNyQOA7DJaXA)