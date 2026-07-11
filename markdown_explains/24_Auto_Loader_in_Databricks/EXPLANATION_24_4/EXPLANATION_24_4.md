# EXPLANATION 24 4

**Question 4**

**What is the primary purpose of the checkpoint directory?**

**Correct Answer:** **C. To store progress, schema information, processed file metadata, and RocksDB data**

**Explanation**

The checkpoint directory stores everything needed for fault tolerance and recovery:

- Streaming progress

- Offsets

- RocksDB metadata

- Processed file metadata

- Schema tracking

If the stream fails, it resumes from the checkpoint rather than starting over.

**YouTube**

- https://www.youtube.com/results?search_query=Databricks+checkpoint+Structured+Streaming

- https://www.youtube.com/results?search_query=Auto+Loader+checkpoint+Databricks

------------------------------------------------------------------------

# [README](./../../../README.md)
