# ANSWER 42 4

**Question 4**

**Which component is required to create Streaming Tables and Materialized Views directly in Databricks SQL?**

**A. Spark Driver Node** ❌ Incorrect

- Users don't interact directly with driver nodes in DBSQL.

**B. Unity Catalog Metastore** ❌ Incorrect

- Unity Catalog manages metadata.

- It is not the SQL execution engine.

**C. SQL Warehouse** ✅ Correct

- SQL statements execute on a SQL Warehouse.

- Therefore, creating:

  - Streaming Tables

  - Materialized Views\
    requires an active SQL Warehouse.

**D. MLflow Server** ❌ Incorrect

- MLflow manages machine learning.

**E. Databricks Workflow Job** ❌ Incorrect

- Workflows schedule execution.

- They are not required simply to create these objects.

**Key Concept**

**DBSQL Objects execute on SQL Warehouses**

# [README](./../../../README.md)
