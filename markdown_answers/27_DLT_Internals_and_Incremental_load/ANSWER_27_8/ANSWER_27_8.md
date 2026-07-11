# ANSWER 27 8

**Question 8**

**Where is the physical data for DLT Streaming Tables and Materialized Views actually stored?**

**A. Only inside notebook files ❌ Incorrect**

- Notebooks contain code, not stored data.

------------------------------------------------------------------------

**B. In Azure SQL Database ❌ Incorrect**

- DLT stores data in Delta tables, not Azure SQL.

------------------------------------------------------------------------

**C. In hidden Delta tables within the Databricks Internal Catalog managed by DLT ✅ Correct**

DLT manages physical storage behind the scenes.

Conceptually:

DLT Pipeline

↓

Hidden Delta Tables

↓

Streaming Tables

Materialized Views

Developers work with logical datasets while DLT manages the underlying Delta tables.

------------------------------------------------------------------------

**D. Only in Unity Catalog metadata tables ❌ Incorrect**

- Unity Catalog stores metadata, not the physical table data.

------------------------------------------------------------------------

**E. Inside Spark executor memory only ❌ Incorrect**

- Executor memory is temporary.

- DLT stores persistent Delta data on storage.

------------------------------------------------------------------------

**Why C is correct**

The physical data resides in hidden Delta tables that DLT manages automatically.

------------------------------------------------------------------------

# [README](./../../../README.md)
