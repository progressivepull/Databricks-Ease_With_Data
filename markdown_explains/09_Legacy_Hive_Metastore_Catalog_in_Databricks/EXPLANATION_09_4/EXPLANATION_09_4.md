# EXPLANATION 09 4

**Question 4**

**Which statement correctly describes a managed table in the Hive Metastore?**

**Correct Answer:**\
✅ **Databricks manages both the table metadata and the physical data files.**

**Explanation**

A **managed table** is completely managed by Databricks.

Databricks controls:

- Metadata

- Storage location

- Physical files

- Cleanup when the table is dropped

Example:

CREATE TABLE\
\
↓\
\
Databricks Chooses Storage\
\
↓\
\
Data Stored\
\
↓\
\
DROP TABLE\
\
↓\
\
Metadata Deleted\
\
↓\
\
Files Deleted

Because Databricks owns the table, it is responsible for both the metadata and the underlying files.

**YouTube**

**Managed vs External Tables**

https://www.youtube.com/results?search_query=Databricks+Managed+vs+External+Tables

# [README](./../../../README.md)
