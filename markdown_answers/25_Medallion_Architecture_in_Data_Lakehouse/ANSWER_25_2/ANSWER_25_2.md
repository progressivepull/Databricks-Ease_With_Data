# ANSWER 25 2

**Question 2**

**Which Structured Streaming source does Auto Loader use to read incoming files?**

**A. deltaFiles ❌ Incorrect**

There is no Structured Streaming source called **deltaFiles**.

Streaming from Delta tables uses:

.format("delta")

------------------------------------------------------------------------

**B. cloudFiles ✅ Correct**

Example:

spark.readStream \\

.format("cloudFiles")

The **cloudFiles** source provides:

- automatic file discovery

- schema inference

- schema evolution

- notification support

- scalable ingestion

It is the heart of Auto Loader.

------------------------------------------------------------------------

**C. autoStream ❌ Incorrect**

No such Structured Streaming source exists.

------------------------------------------------------------------------

**D. fileLoader ❌ Incorrect**

No such source exists.

------------------------------------------------------------------------

**E. streamFiles ❌ Incorrect**

Also not a valid Spark source.

------------------------------------------------------------------------

**Why B is correct**

Auto Loader is simply the **cloudFiles** source built on Structured Streaming.

------------------------------------------------------------------------

# [README](./../../../README.md)
