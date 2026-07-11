# ANSWER 24 1

**Question 1**

**What is the primary purpose of Auto Loader in Databricks?**

**A. To manually copy files from local machines into DBFS** ❌ Incorrect

- Auto Loader is **not** designed for manually uploading files.

- Manual uploads are typically done through the Databricks UI, DBFS commands, or dbutils.fs.cp.

- Auto Loader continuously monitors cloud storage for new files.

- **Key point:** Manual file copying is outside Auto Loader's purpose.

------------------------------------------------------------------------

**B. To efficiently and incrementally ingest new files from cloud storage into Delta Lake tables** ✅ Correct

- This is exactly what Auto Loader was built for.

- It continuously detects newly arriving files.

- It only processes files that have not been processed before.

- It supports:

  - Amazon S3

  - Azure Data Lake Storage (ADLS)

  - Google Cloud Storage (GCS)

  - DBFS

  - Unity Catalog Volumes

- It is optimized for millions of files.

**Think of it like this:**

Auto Loader is a smart mail carrier. Every day it checks the mailbox and only delivers the new letters.

------------------------------------------------------------------------

**C. To replace Unity Catalog metadata management** ❌ Incorrect

- Unity Catalog manages:

  - Catalogs

  - Schemas

  - Tables

  - Permissions

  - Governance

- Auto Loader only ingests data.

- They solve completely different problems.

------------------------------------------------------------------------

**D. To optimize SQL query performance on Delta tables** ❌ Incorrect

- SQL performance is improved through:

  - SQL Warehouses

  - Photon

  - Delta Lake optimizations

  - ZORDER

  - OPTIMIZE

- Auto Loader loads data.

- It does **not** speed up SQL queries.

------------------------------------------------------------------------

**E. To create Spark clusters automatically** ❌ Incorrect

- Clusters are created by:

  - Compute

  - Jobs

  - Workflows

- Auto Loader runs **on** Spark clusters.

- It does not create them.

------------------------------------------------------------------------

**Why B is correct**

Auto Loader's mission is:

Efficient, scalable, incremental ingestion of new files into Delta Lake.

------------------------------------------------------------------------

# [README](./../../../README.md)
