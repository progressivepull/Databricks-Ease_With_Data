# EXPLANATION 26 4

**Question 4**

**Which method is typically used to read data that will populate a Streaming Table in DLT?**

**Correct Answer:** **C. spark.readStream.table()**

**Explanation**

Streaming Tables require streaming input.

spark.readStream.table("bronze")

creates a streaming DataFrame that continuously receives new data.

**Why the Correct Answer is Correct**

readStream continuously monitors the source for new records.

**Why the Other Answers Are Wrong**

- spark.read.table() performs a one-time batch read.

- Other methods are not intended for streaming ingestion.

**YouTube Video**

**Direct Link**\
[<u>https://www.youtube.com/watch?v=iqf_QHC7tgQ</u>](https://www.youtube.com/watch?v=iqf_QHC7tgQ)

**YouTube Search**\
https://www.youtube.com/results?search_query=spark.readStream.table+Databricks

# [README](./../../../README.md)
