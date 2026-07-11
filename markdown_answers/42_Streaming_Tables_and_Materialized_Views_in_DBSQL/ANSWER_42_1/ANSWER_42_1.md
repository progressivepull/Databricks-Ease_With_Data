# ANSWER 42 1

**Question 1**

**What is the primary purpose of a Streaming Table in Databricks SQL (DBSQL)?**

**A. To permanently archive Delta transaction logs** ❌ Incorrect

- Delta transaction logs (\_delta_log) record changes made to Delta tables.

- Streaming Tables do **not** archive these logs.

- Delta Lake manages transaction logs automatically.

**B. To continuously ingest incremental data from a streaming source** ✅ Correct

- This is the primary purpose of a Streaming Table.

- It continuously processes **newly arriving data** from sources such as:

  - Unity Catalog Volumes

  - Cloud storage (ADLS, S3, GCS)

  - Other streaming sources

- Instead of repeatedly processing all data, it processes only new data after the initial load.

Example:

Cloud Storage

│

New CSV Files

│

Streaming Table

│

Delta Table

**C. To replace SQL Warehouses for query execution** ❌ Incorrect

- SQL Warehouses execute SQL queries.

- Streaming Tables store and update data.

- They serve different purposes.

**D. To store only precomputed aggregations for dashboards** ❌ Incorrect

- That describes a **Materialized View**, not a Streaming Table.

**E. To automatically create Unity Catalog catalogs** ❌ Incorrect

- Unity Catalog catalogs are created separately using SQL commands.

- Streaming Tables don't manage catalog creation.

**Key Concept**

**Streaming Table = Continuous incremental data ingestion**

# [README](./../../../README.md)
