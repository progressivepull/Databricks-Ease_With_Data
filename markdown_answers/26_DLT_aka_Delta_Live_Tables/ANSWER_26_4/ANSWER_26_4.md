# ANSWER 26 4

**Question 4**

**Which method is typically used to read data that will populate a Streaming Table in DLT?**

**A. spark.sql() ❌ Incorrect**

Runs SQL queries.

Not a streaming reader.

**B. spark.read.table() ❌ Incorrect**

Reads tables in batch mode.

Processes existing data only.

**C. spark.readStream.table() ✅ Correct**

Example:

spark.readStream.table("bronze_orders")

This continuously reads new records as they arrive.

Perfect for Streaming Tables.

**D. spark.read.csv() ❌ Incorrect**

Reads CSV files once.

Batch processing.

**E. spark.table() ❌ Incorrect**

Also performs batch reads.

Not streaming.

**Why C is correct**

Streaming Tables require a streaming source, and spark.readStream.table() provides continuous ingestion.

# [README](./../../../README.md)
