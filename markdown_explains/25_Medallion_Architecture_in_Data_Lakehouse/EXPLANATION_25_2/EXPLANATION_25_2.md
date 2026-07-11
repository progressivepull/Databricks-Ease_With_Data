# EXPLANATION 25 2

**Question 2**

**Which technology is Auto Loader built on?**

**Correct Answer**

✅ **C. Structured Streaming using the CloudFiles source**

**Explanation**

Auto Loader is not its own processing engine.

Instead it is built on:

- Apache Spark Structured Streaming

- using the special source:

.format("cloudFiles")

Example:

spark.readStream \\

.format("cloudFiles")

CloudFiles is what gives Structured Streaming the ability to watch cloud storage.

**Easy Memory Trick**

CloudFiles = Auto Loader

Structured Streaming + CloudFiles = Auto Loader

**YouTube**

[YouTube video link](https://www.youtube.com/watch?v=d7u5ugwmc0E)

Search

https://www.youtube.com/results?search_query=Databricks+CloudFiles+Structured+Streaming

------------------------------------------------------------------------

# [README](./../../../README.md)
