# ANSWER 23 10

**Question 10**

**According to the lesson, when should Auto Loader generally be preferred over COPY INTO?**

**A. When loading a few CSV files once a month** ❌ Incorrect

- COPY INTO is ideal for small, occasional batch loads.

**B. When processing small batch workloads with hundreds of files** ❌ Incorrect

- COPY INTO is still a good fit for this scenario.

**C. When handling millions of continuously arriving files and complex directory structures** ✅ Correct

Auto Loader is designed for:

- Massive file volumes

- Continuous ingestion

- Streaming-like processing

- Efficient file discovery

- Complex directory hierarchies

Example:

Millions of Files\
\
↓\
\
Auto Loader\
\
↓\
\
Continuous Processing

This is where Auto Loader clearly outperforms COPY INTO.

**D. When creating placeholder Delta tables** ❌ Incorrect

- Placeholder tables are a COPY INTO pattern.

**E. When reading data from Unity Catalog volumes only** ❌ Incorrect

- COPY INTO can also read from Unity Catalog Volumes.

**Memory Trick**

Small Batch

↓

COPY INTO

Large Continuous Ingestion

↓

Auto Loader

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| Purpose of COPY INTO | Load files from cloud storage or Unity Catalog Volumes into Delta tables |
| Supported formats | CSV, JSON, Parquet, Avro, Text, and Binary files |
| Idempotent | Previously processed files are automatically skipped when the command is run again |
| Placeholder table | Empty Delta table that allows COPY INTO to infer the schema automatically |
| Automatic column creation | **Schema Inference** |
| Tracks processed files | Delta transaction log (\_delta_log) |
| Simple transformations | Wrap the source in a SELECT statement during COPY INTO |
| New file arrives | Only the new file is loaded; previously processed files are skipped |
| Handle schema changes | **Schema Evolution** |
| Use Auto Loader instead | Large-scale, continuously arriving data with millions of files or complex directory structures |

# [README](./../../../README.md)
