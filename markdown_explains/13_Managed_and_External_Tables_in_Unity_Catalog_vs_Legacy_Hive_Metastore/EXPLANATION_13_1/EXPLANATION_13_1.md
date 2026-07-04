# EXPLANATION 13 1

**Question 1**

**Before creating an external table in Unity Catalog, what must first be created in Azure Data Lake Storage (ADLS)?**

**Correct Answer:**\
✅ **A dedicated storage folder for external table data**

**Explanation**

An **external table** stores its data in a location that **you own and manage**. Unlike a managed table, Unity Catalog does **not** choose or create the storage location for you.

Before creating the external table, you should create a folder in ADLS Gen2, for example:

ADLS Gen2\
│\
└── sales-data/\
├── 2026/\
├── 2027/\
└── invoices.parquet

When you create the table, you reference this folder:

CREATE EXTERNAL TABLE sales\
LOCATION 'abfss://sales@storageaccount.dfs.core.windows.net/sales-data/';

The folder already exists; Unity Catalog simply registers it.

**Why?**

Because the customer owns:

- The storage account

- The folder

- The files

Unity Catalog only manages the metadata.

Databricks documents that external tables reference customer-managed cloud storage locations.

**YouTube**

**Unity Catalog External Tables**

https://www.youtube.com/results?search_query=Unity+Catalog+External+Tables

# [README](./../../../README.md)
