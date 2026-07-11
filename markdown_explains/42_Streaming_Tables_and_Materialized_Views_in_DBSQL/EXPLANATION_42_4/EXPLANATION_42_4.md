# EXPLANATION 42 4

**Question 4**

**Which component is required to create Streaming Tables and Materialized Views directly in Databricks SQL?**

**Correct Answer:**\
**C. SQL Warehouse**

**Why C is Correct**

All Databricks SQL statements execute on a **SQL Warehouse**.

When creating Streaming Tables or Materialized Views from DBSQL:

- SQL Warehouse parses the SQL.

- Executes the DDL statements.

- Coordinates with Lakeflow/DLT.

Without an active SQL Warehouse, DBSQL cannot execute the SQL commands.

**Why the other choices are wrong**

- Unity Catalog stores metadata.

- Delta Lake stores data.

- Photon accelerates execution.

- None replace the SQL Warehouse.

**Memory Tip**

**DBSQL always runs on a SQL Warehouse.**

**Individual YouTube Video**

Databricks SQL Warehouse Overview

[https://www.youtube.com/watch?v=zi3RCZVsQDs](https://www.youtube.com/watch?v=zi3RCZVsQDs&utm_source=chatgpt.com)

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+SQL+Warehouse

------------------------------------------------------------------------

# [README](./../../../README.md)
