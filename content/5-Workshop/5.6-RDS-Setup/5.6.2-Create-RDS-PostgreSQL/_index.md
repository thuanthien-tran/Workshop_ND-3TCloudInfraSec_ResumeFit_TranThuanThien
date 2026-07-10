---
title: "5.6.2 Database Instance Initialization"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.6.2. Database Instance Initialization

1. Navigate to the **RDS** Console, go to **Subnet groups** and create a group named `resumematching-dbsubnetgroup` containing `Private-DB-A` and `Private-DB-B` subnets.
   ![Create DB Subnet Group](/images/5-Workshop/Tao_DB_Subnet_Group.jpg)

2. Create a new Database instance (DB identifier: `resume-matching-db`) running **PostgreSQL** engine on class `db.t3.micro`.
   ![Create RDS Instance](/images/5-Workshop/Tao_RDS_database.jpg)
