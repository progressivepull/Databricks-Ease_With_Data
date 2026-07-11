# EXPLANATION 24 2

**Question 2**

**Which technology is Auto Loader built on?**

**Correct Answer:** **C. Structured Streaming using the CloudFiles source**

**Explanation**

Auto Loader is built on **Apache Spark Structured Streaming**.

Instead of using:

spark.read()

it uses:

spark.readStream()

combined with the special **CloudFiles** source:

.format("cloudFiles")

CloudFiles provides:

- Incremental file discovery

- Schema inference

- Schema evolution

- Scalable metadata tracking

**YouTube**

- https://www.youtube.com/results?search_query=Databricks+Structured+Streaming+Auto+Loader

- https://www.youtube.com/results?search_query=CloudFiles+Auto+Loader+Databricks

------------------------------------------------------------------------

# [README](./../../../README.md)
