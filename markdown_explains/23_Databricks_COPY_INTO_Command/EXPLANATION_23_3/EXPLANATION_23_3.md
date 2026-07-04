# EXPLANATION 23 3

**Question 2**

**Which of the following file formats is supported by the COPY INTO command?**

**Correct Answer: B. CSV, JSON, Parquet, Avro, Text, and Binary files**

**Explanation**

COPY INTO supports many common data formats, including:

- CSV

- JSON

- Parquet

- Avro

- Text

- Binary

Examples:

CSV

COPY INTO sales\
FROM '/Volumes/raw/sales'\
FILEFORMAT = CSV;

JSON

COPY INTO customers\
FROM '/Volumes/raw/customers'\
FILEFORMAT = JSON;

Parquet

COPY INTO orders\
FROM '/Volumes/raw/orders'\
FILEFORMAT = PARQUET;

This flexibility makes COPY INTO useful for many ingestion scenarios.

**YouTube**

- **Databricks Data Ingestion Formats**\
  https://www.youtube.com/results?search_query=Databricks+CSV+JSON+Parquet+COPY+INTO

# [README](./../../../README.md)
