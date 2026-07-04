# EXPLANATION 09 7

**Question 7**

**What happens when a managed table is dropped?**

**Correct Answer:**\
✅ **Both the metadata and physical data files are deleted.**

**Explanation**

Managed tables are owned by Databricks.

Dropping one removes:

- Metadata

- Physical files

Workflow:

DROP TABLE\
\
↓\
\
Delete Metadata\
\
↓\
\
Delete Files

This behavior differs from external tables, where only the metadata is removed.

**Note:** This describes the traditional Hive Metastore behavior. Unity Catalog managed tables add a recovery window with UNDROP TABLE, changing the deletion behavior.

**YouTube**

**Databricks Managed Tables**

https://www.youtube.com/results?search_query=Databricks+Managed+Tables

# [README](./../../../README.md)
