# ANSWER 09 5

**Question 5**

**Where are managed table data files stored by default in the Hive Metastore?**

**A. Amazon S3 only** ❌ Incorrect

- Databricks runs on AWS, Azure, and GCP.

- Hive Metastore is not limited to S3.

**B. Azure Key Vault** ❌ Incorrect

- Key Vault stores secrets.

- It does not store table data.

**C. DBFS (Databricks File System)** ✅ Correct

Traditionally, Hive Metastore managed tables stored data under DBFS.

Example:

dbfs:/user/hive/warehouse/

Databricks automatically manages this location.

**D. Unity Catalog Volumes** ❌ Incorrect

- Volumes belong to Unity Catalog.

**E. Git repositories** ❌ Incorrect

- Git stores source code, not data files.

**Key Concept**

Traditional Hive Metastore:

Managed Table\
│\
▼\
DBFS

------------------------------------------------------------------------

# [README](./../../../README.md)
