# EXPLANATION 42 1

**Question 1**

**What is the primary purpose of a Streaming Table in Databricks SQL (DBSQL)?**

**Correct Answer:**\
**B. To continuously ingest incremental data from a streaming source**

**Why B is Correct**

A **Streaming Table** is designed to continuously ingest new data as it arrives. Instead of reprocessing the entire dataset every time, it performs **incremental processing**, loading only newly detected records.

Streaming Tables are ideal for:

- Event streams

- Log files

- IoT sensor data

- CDC (Change Data Capture)

- Incremental file ingestion

This provides near real-time analytics while avoiding unnecessary work.

**Why the other choices are wrong**

- **A.** Streaming Tables are not primarily for batch-only processing.

- **C.** They do not replace Delta tables; they are built on Delta Lake.

- **D.** They are not used for machine learning model training.

- **E.** They do not replace SQL Warehouses.

**Memory Tip**

**Streaming Table = New data only**

**Individual YouTube Video**

Databricks Streaming Tables Overview

https://www.youtube.com/watch?v=lR1Q3F2M4qI

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Streaming+Tables

# [README](./../../../README.md)
