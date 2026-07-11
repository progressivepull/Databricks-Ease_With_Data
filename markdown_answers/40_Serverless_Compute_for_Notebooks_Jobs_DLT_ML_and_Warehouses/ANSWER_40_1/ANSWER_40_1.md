# ANSWER 40 1

**Question 1**

**What is the primary purpose of Databricks Serverless Compute?**

**A. To require users to manually configure Spark clusters before running code** ❌ Incorrect

- This describes the **traditional (Classic Compute)** experience.

- With Classic Compute, users often choose cluster size, runtime version, autoscaling, and other settings.

- **Serverless removes most of this manual cluster management.**

**B. To automatically manage compute infrastructure, including cluster creation, scaling, and termination** ✅ Correct

- This is exactly what Serverless Compute is designed to do.

- Databricks automatically:

  - Creates compute when needed

  - Scales resources up and down

  - Terminates compute when idle

- Users focus on writing code rather than managing infrastructure.

**C. To replace Unity Catalog with a new governance system** ❌ Incorrect

- Unity Catalog handles:

  - Data governance

  - Permissions

  - Catalogs

  - Schemas

  - Lineage

- Serverless Compute is only about **compute**, not governance.

**D. To permanently store Delta Lake tables** ❌ Incorrect

- Delta tables are stored in cloud storage (ADLS, S3, GCS).

- Serverless Compute processes the data but does **not** store it.

**E. To eliminate the need for Databricks SQL Warehouses** ❌ Incorrect

- SQL Warehouses still exist.

- In fact, **Serverless SQL Warehouses** are one of the Serverless offerings.

**Key Concept**

Serverless Compute automates infrastructure management so users only worry about their workloads.

# [README](./../../../README.md)
