# ANSWER 42 5

**Question 5**

**Which SQL function is demonstrated for reading CSV files from Unity Catalog Volumes and cloud storage?**

**A. LOAD_DATA()** ❌ Incorrect

- Not a Databricks SQL function.

**B. COPY_FILES()** ❌ Incorrect

- No such SQL function exists.

**C. READ_FILES()** ✅ Correct

- READ_FILES() reads files directly from:

  - Unity Catalog Volumes

  - Cloud Storage

- It supports formats like:

  - CSV

  - JSON

  - Parquet

Example:

SELECT \*

FROM READ_FILES('/Volumes/catalog/schema/data/')

**D. STREAM_SOURCE()** ❌ Incorrect

- Not a Databricks SQL function.

**E. IMPORT_TABLE()** ❌ Incorrect

- No such SQL function exists.

**Key Concept**

**READ_FILES() reads files directly into SQL queries.**

# [README](./../../../README.md)
