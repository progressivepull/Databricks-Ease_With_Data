# EXPLANATION 14 4

**Question 4**

**Which command displays the transaction history of a Delta table?**

**Correct Answer:**\
✅ **DESCRIBE HISTORY table_name;**

**Explanation**

Every Delta table keeps a transaction log.

Example:

DESCRIBE HISTORY sales.orders;

Returns information such as:

- Version

- Timestamp

- User

- Operation

- Notebook

- Cluster

- Operation Metrics

Example:

Version 15\
\
MERGE\
\
User: John\
\
Rows Updated: 250

This history is stored in the Delta transaction log (\_delta_log) and is one of Delta Lake's key features.

**YouTube**

**Delta Lake History**

https://www.youtube.com/results?search_query=Databricks+DESCRIBE+HISTORY

# [README](./../../../README.md)
