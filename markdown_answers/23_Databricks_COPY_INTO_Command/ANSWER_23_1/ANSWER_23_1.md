# ANSWER 23 1

**Question 1**

**What is the primary purpose of the COPY INTO command in Databricks?**

**A. To optimize Delta tables** ❌ Incorrect

- Table optimization is performed with:

> OPTIMIZE table_name;

- COPY INTO loads data—it does **not** optimize storage.

**B. To ingest files from cloud storage or Unity Catalog volumes into Delta tables** ✅ Correct

COPY INTO is a data ingestion command.

It reads files from locations such as:

- Azure Data Lake Storage (ADLS)

- Amazon S3

- Google Cloud Storage (GCS)

- Unity Catalog Volumes

and loads them into a Delta table.

Example:

CSV Files\
\
↓\
\
COPY INTO\
\
↓\
\
Delta Table

This is commonly used for batch ingestion.

**C. To create Spark clusters automatically** ❌ Incorrect

- Clusters are compute resources.

- COPY INTO only loads data.

**D. To replace Auto Loader in all scenarios** ❌ Incorrect

- Auto Loader is better for continuous, high-volume ingestion.

- COPY INTO is best for simpler batch ingestion.

**E. To manage Unity Catalog permissions** ❌ Incorrect

- Permissions are handled by Unity Catalog.

**Memory Trick**

COPY INTO

↓

Copy Files

↓

Delta Table

# [README](./../../../README.md)
