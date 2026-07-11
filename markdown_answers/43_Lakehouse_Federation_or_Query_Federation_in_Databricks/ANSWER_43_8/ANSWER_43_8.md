# ANSWER 43 8

**Question 8**

**How does Databricks query data in a Foreign Catalog?**

**A. It requires a special SQL dialect different from ANSI SQL.** ❌ Incorrect

- One of the biggest advantages is that users continue writing standard ANSI SQL.

**B. It first imports all tables into Delta Lake before querying.** ❌ Incorrect

- That would defeat the purpose of Federation.

**C. It uses the same SQL syntax as native Unity Catalog tables while reading data from the external database.** ✅ Correct

- Users query external tables just like native Databricks tables.

Example:

SELECT \*

FROM foreign_catalog.sales.orders;

The SQL syntax is the same.

**D. It converts the external database into a Streaming Table automatically.** ❌ Incorrect

- Federation does not convert databases.

**E. It only supports Python notebooks for querying external data.** ❌ Incorrect

- SQL Warehouses and SQL notebooks fully support Federation.

**Key Concept**

**Same SQL syntax, different storage location.**

# [README](./../../../README.md)
