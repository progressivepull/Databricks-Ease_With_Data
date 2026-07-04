# EXPLANATION 09 5

**Question 5**

**Where are managed table data files stored by default in the Hive Metastore?**

**Correct Answer:**\
✅ **DBFS (Databricks File System)**

**Explanation**

Traditionally, Hive Metastore managed tables stored their data under the Databricks File System (DBFS).

Typical location:

dbfs:/user/hive/warehouse/

DBFS provides a filesystem abstraction over cloud object storage and was the default location for managed tables in the legacy Hive Metastore model.

**Note:** Modern Unity Catalog deployments typically use managed cloud storage locations (such as ADLS Gen2, S3, or GCS) instead of relying on DBFS for managed tables.

**YouTube**

**Databricks DBFS Explained**

https://www.youtube.com/results?search_query=Databricks+DBFS+Tutorial

# [README](./../../../README.md)
