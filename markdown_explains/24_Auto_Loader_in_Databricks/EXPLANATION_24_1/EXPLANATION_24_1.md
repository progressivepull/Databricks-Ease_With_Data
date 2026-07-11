# EXPLANATION 24 1

**Question 1**

**What is the primary purpose of Auto Loader in Databricks?**

**Correct Answer:** **B. To efficiently and incrementally ingest new files from cloud storage into Delta Lake tables**

**Explanation**

Auto Loader is Databricks' recommended file ingestion framework.

Instead of repeatedly loading every file in a folder, Auto Loader keeps track of which files have already been processed and loads only new files as they arrive. It is designed for cloud object storage such as ADLS, Amazon S3, Google Cloud Storage, Azure Blob Storage, and Unity Catalog Volumes, and can scale to millions of new files per hour.

**Example**

Cloud Storage

│

New CSV Files

│

Auto Loader

│

Delta Lake Table

**YouTube**

- **Databricks Official – How Databricks Leverages Auto Loader to Ingest Millions of Files an Hour**\
  https://www.youtube.com/results?search_query=How+Databricks+Leverages+Auto+Loader+to+Ingest+Millions+of+Files+an+Hour

- **Auto Loader Tutorial**\
  https://www.youtube.com/results?search_query=Databricks+Auto+Loader+Tutorial

------------------------------------------------------------------------

# [README](./../../../README.md)
