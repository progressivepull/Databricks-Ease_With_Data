# EXPLANATION 17 1

**Question 1**

**What is the primary purpose of Volumes in Unity Catalog?**

**Correct Answer:**\
✅ **To provide governed storage for structured, semi-structured, and unstructured files**

**Explanation**

Before Unity Catalog Volumes were introduced, Databricks users often stored non-tabular files in locations such as:

- DBFS

- Mounted storage

- Direct cloud storage paths

Those approaches lacked the centralized governance provided by Unity Catalog.

**Unity Catalog Volumes** solve this by providing a governed location for files.

Volumes can store almost any type of file, including:

**Structured Data**

- CSV

- Parquet

**Semi-Structured Data**

- JSON

- XML

- Avro

**Unstructured Data**

- Images

- PDFs

- Videos

- ZIP files

- Machine Learning models

- Text files

Unlike Delta tables, Volumes are intended for **file storage**, not relational tables.

**Architecture**

Metastore\
│\
▼\
Catalog\
│\
▼\
Schema\
├── Tables\
├── Views\
├── Functions\
└── Volume\
│\
├── Images\
├── PDFs\
├── CSV\
└── ML Models

Databricks documents Volumes as Unity Catalog objects for governing access to non-tabular data.

**YouTube**

**Unity Catalog Volumes**

https://www.youtube.com/results?search_query=Unity+Catalog+Volumes

# [README](./../../../README.md)
