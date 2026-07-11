# EXPLANATION 42 5

**Question 5**

**Which SQL function is demonstrated for reading CSV files from Unity Catalog Volumes and cloud storage?**

**Correct Answer:**\
**C. READ_FILES()**

**Why C is Correct**

READ_FILES() is a Databricks SQL table-valued function that reads files directly from supported storage locations.

It supports formats such as:

- CSV

- JSON

- Parquet

- Avro

- ORC

- Text

It is commonly demonstrated when creating Streaming Tables that ingest files from Unity Catalog Volumes or cloud object storage.

**Why the other choices are wrong**

Functions like SELECT, COPY INTO, or LOAD DATA serve different purposes and are not the SQL function highlighted in this lesson.

**Memory Tip**

**READ_FILES() = Read files directly**

**Individual YouTube Video**

READ_FILES Databricks SQL Demo

https://www.youtube.com/watch?v=WWM4Y8R7n8Q

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+READ_FILES+SQL

------------------------------------------------------------------------

# [README](./../../../README.md)
