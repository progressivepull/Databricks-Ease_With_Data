# ANSWER 24 2

**Question 2**

**Which technology is Auto Loader built on?**

**A. Delta Live Tables only** ❌ Incorrect

- DLT can use Auto Loader.

- Auto Loader is not built on DLT.

- DLT is a higher-level pipeline framework.

Think:

DLT

↓

Auto Loader

↓

Structured Streaming

------------------------------------------------------------------------

**B. Databricks SQL Warehouses** ❌ Incorrect

- SQL Warehouses run analytical SQL.

- They don't ingest files.

------------------------------------------------------------------------

**C. Structured Streaming using the CloudFiles source** ✅ Correct\
Auto Loader is built directly on:

Spark Structured Streaming

\+

CloudFiles source

Example:

spark.readStream.format("cloudFiles")

CloudFiles adds:

- incremental file discovery

- schema inference

- schema evolution

- notification support

------------------------------------------------------------------------

**D. Apache Kafka Connect** ❌ Incorrect\
Kafka Connect ingests streaming events.

Auto Loader ingests files.

Different technologies.

------------------------------------------------------------------------

**E. MLflow Tracking** ❌ Incorrect\
MLflow tracks:

- experiments

- models

- metrics

Nothing related to file ingestion.

------------------------------------------------------------------------

**Why C is correct**

Auto Loader extends Structured Streaming with the CloudFiles source.

------------------------------------------------------------------------

# [README](./../../../README.md)
