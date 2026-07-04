# EXPLANATION 14 1

**Question 1**

**Which SQL command lists all catalogs available in Unity Catalog?**

**Correct Answer:**\
✅ **SHOW CATALOGS;**

**Explanation**

A **Catalog** is the highest-level data container inside Unity Catalog (below the metastore).

To see every catalog you have permission to access, use:

SHOW CATALOGS;

Example output:

main\
finance\
sales\
hr\
marketing

This command only works with **Unity Catalog** because catalogs are part of Unity Catalog's three-level namespace. If no filter is provided, it lists all catalogs in the metastore that you have permission to see.

**Unity Catalog Hierarchy**

Metastore\
│\
▼\
Catalog\
│\
▼\
Schema\
│\
▼\
Table

**Useful SQL**

SHOW CATALOGS;\
\
USE CATALOG finance;\
\
SHOW SCHEMAS;\
\
SHOW TABLES;

**YouTube**

**Unity Catalog SQL Commands**

https://www.youtube.com/results?search_query=Databricks+SHOW+CATALOGS+Unity+Catalog

# [README](./../../../README.md)
