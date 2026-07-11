# EXPLANATION 25 1

**Question 1**

**What is the primary purpose of Auto Loader in Databricks?**

**Correct Answer:**\
✅ **B. To efficiently and incrementally ingest new files from cloud storage into Delta Lake tables**

**Explanation**

Auto Loader is Databricks' scalable file ingestion engine.

Its job is to:

- Monitor cloud storage

- Detect newly arriving files

- Load only new files

- Write data into Delta Lake

Unlike a normal batch load, Auto Loader remembers what has already been processed.

Supported storage includes:

- Azure Data Lake Storage (ADLS)

- Amazon S3

- Google Cloud Storage

- Unity Catalog Volumes

- DBFS

It is designed to process millions (or billions) of files efficiently.

**Easy Memory Trick**

**Auto Loader = Smart File Watcher**

It keeps watching cloud storage and loads only new files.

**YouTube**

Official Databricks Auto Loader Deep Dive

[YouTube video link](https://www.youtube.com/watch?v=z6YmbwFgq88)

Search Results

https://www.youtube.com/results?search_query=Databricks+Auto+Loader

------------------------------------------------------------------------

# [README](./../../../README.md)
