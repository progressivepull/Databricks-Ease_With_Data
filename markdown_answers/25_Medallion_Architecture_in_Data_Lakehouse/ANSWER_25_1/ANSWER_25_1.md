# ANSWER 25 1

**Question 1**

**What is the primary purpose of Databricks Auto Loader?**

**A. To create Delta Lake tables from SQL scripts only ❌ Incorrect**

- Auto Loader is **not** a SQL tool.

- Delta tables can be created using SQL (CREATE TABLE) without Auto Loader.

- Auto Loader's responsibility is **loading files into Delta tables**, not creating tables from SQL scripts.

------------------------------------------------------------------------

**B. To continuously optimize Delta tables for performance ❌ Incorrect**

- Table optimization is handled by:

  - OPTIMIZE

  - VACUUM

  - Z-Ordering

  - Predictive Optimization

- Auto Loader only **loads data**.

- It does **not** optimize storage or query performance.

------------------------------------------------------------------------

**C. To incrementally ingest new files from cloud storage into Delta Lake tables ✅ Correct**

This is exactly why Auto Loader exists.

It:

- Watches cloud storage.

- Detects new files.

- Loads only files that have never been processed.

- Supports:

  - Azure Data Lake Storage (ADLS)

  - Amazon S3

  - Google Cloud Storage (GCS)

  - DBFS

  - Unity Catalog Volumes

Think of Auto Loader like an employee checking a mailbox every few minutes:

- Old letters → ignored

- New letters → delivered

That is **incremental ingestion**.

------------------------------------------------------------------------

**D. To replace Structured Streaming with batch processing ❌ Incorrect**

Actually, Auto Loader is **built on Structured Streaming**.

It does not replace it.

Architecture:

Spark Structured Streaming

↓

cloudFiles source

↓

Auto Loader

------------------------------------------------------------------------

**E. To convert Parquet files into CSV files automatically ❌ Incorrect**

Auto Loader does not convert file formats.

It reads formats like:

- CSV

- JSON

- Parquet

- Avro

- XML

- ORC

- Text

and loads them into Delta tables.

------------------------------------------------------------------------

**Why C is correct**

Auto Loader's entire purpose is:

Efficient, scalable, incremental ingestion of newly arriving files into Delta Lake.

------------------------------------------------------------------------

# [README](./../../../README.md)
