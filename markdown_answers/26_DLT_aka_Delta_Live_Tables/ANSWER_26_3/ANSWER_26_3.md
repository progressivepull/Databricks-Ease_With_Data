# ANSWER 26 3

**Question 3**

**Which DLT dataset type is designed for continuously arriving data and incremental processing?**

**A. View ❌ Incorrect**

Views are temporary transformations.

They are not stored permanently.

They are not intended for continuous streaming ingestion.

**B. Materialized View ❌ Incorrect**

Materialized Views store computed results.

They are typically refreshed rather than continuously ingesting streaming data.

**C. Temporary Table ❌ Incorrect**

A temporary table is session-scoped and unrelated to DLT streaming pipelines.

**D. Streaming Table ✅ Correct**

Streaming Tables are built specifically for:

- continuously arriving data

- incremental processing

- Structured Streaming

Examples:

- IoT sensors

- clickstream

- application logs

- Kafka events

- Auto Loader

**E. Delta Cache ❌ Incorrect**

Delta Cache speeds up reading Delta tables.

It is not a dataset type.

**Why D is correct**

Streaming Tables continuously process new incoming records instead of reprocessing the entire dataset.

# [README](./../../../README.md)
