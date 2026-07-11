# EXPLANATION 24 3

**Question 3**

**How does Auto Loader achieve exactly-once processing?**

**Correct Answer:** **B. By storing processed file metadata in a checkpoint directory using RocksDB**

**Explanation**

Auto Loader guarantees that each file is processed only once.

It stores metadata about processed files in **RocksDB**, a high-performance key-value database located within the checkpoint directory. If the stream restarts, Auto Loader reads this metadata and resumes without reprocessing previously ingested files.

**Example**

Checkpoint

file1.csv ✔

file2.csv ✔

file3.csv ✔

Tomorrow

file4.csv

Only file4.csv loads.

**YouTube**

- https://www.youtube.com/results?search_query=Databricks+Auto+Loader+RocksDB

- https://www.youtube.com/results?search_query=Databricks+Auto+Loader+checkpoint

------------------------------------------------------------------------

# [README](./../../../README.md)
