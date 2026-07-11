# EXPLANATION 25 4

**Question 4**

**What is the primary purpose of the checkpoint directory?**

**Correct Answer**

✅ **C. To store progress, schema information, processed file metadata, and RocksDB data**

**Explanation**

Checkpoint stores everything needed to restart safely.

It includes:

- streaming progress

- offsets

- RocksDB database

- metadata

- schema tracking

- recovery information

If the cluster crashes, Auto Loader resumes from the checkpoint.

**Easy Memory Trick**

Checkpoint = Memory of the stream

**YouTube**

https://www.youtube.com/results?search_query=Databricks+checkpoint+directory+Structured+Streaming

------------------------------------------------------------------------

# [README](./../../../README.md)
