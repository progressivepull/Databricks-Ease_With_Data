# EXPLANATION 23 2

**Question 1**

**What is the primary purpose of the COPY INTO command in Databricks?**

**Correct Answer: B. To ingest files from cloud storage or Unity Catalog volumes into Delta tables**

**Explanation**

COPY INTO reads files from a storage location and loads them into a Delta table.

Supported source locations include:

- Unity Catalog Volumes

- Azure Data Lake Storage (ADLS)

- Amazon S3

- Google Cloud Storage (GCS)

- DBFS (legacy environments)

Example:

COPY INTO sales.orders\
FROM '/Volumes/company/raw/orders'\
FILEFORMAT = CSV;

The command:

1.  Reads the files.

2.  Parses the data.

3.  Writes rows into a Delta table.

4.  Records which files were loaded.

**Real-world example**

Suppose every hour a CSV file arrives:

Landing Folder\
\
employees_001.csv\
employees_002.csv\
employees_003.csv

Running COPY INTO imports the files into a Delta table for analytics.

**YouTube**

- **Databricks COPY INTO Tutorial**\
  https://www.youtube.com/results?search_query=Databricks+COPY+INTO+tutorial

- **Delta Lake Data Ingestion**\
  https://www.youtube.com/results?search_query=Databricks+Delta+Lake+COPY+INTO

# [README](./../../../README.md)
