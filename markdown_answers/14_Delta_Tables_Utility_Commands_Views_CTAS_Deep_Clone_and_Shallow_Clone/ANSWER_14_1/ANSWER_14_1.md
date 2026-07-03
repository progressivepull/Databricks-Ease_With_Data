# ANSWER 14 1

**Question 1**

**Which SQL command lists all catalogs available in Unity Catalog?**

**A. SHOW DATABASES;** ❌ Incorrect

- SHOW DATABASES lists **schemas (databases)** within the current catalog.

- In Unity Catalog, a schema is **not** the same as a catalog.

- Think of it as listing folders inside one cabinet, not all cabinets.

**B. SHOW TABLES;** ❌ Incorrect

- Lists tables in the current schema.

- It does not show catalogs.

**C. SHOW CATALOGS;** ✅ Correct

This command lists every catalog you have permission to see.

Example:

SHOW CATALOGS;

Example output:

main\
sales\
finance\
hr

This is usually one of the first commands people run after enabling Unity Catalog.

**D. LIST CATALOGS;** ❌ Incorrect

- No such SQL command exists in Databricks.

**E. DESCRIBE CATALOGS;** ❌ Incorrect

- DESCRIBE works on a specific catalog.

Example:

DESCRIBE CATALOG EXTENDED sales;

It does **not** list all catalogs.

**Memory Trick**

Hierarchy:

SHOW CATALOGS\
↓\
Catalogs\
\
SHOW DATABASES (Schemas)\
↓\
Schemas\
\
SHOW TABLES\
↓\
Tables

# [README](./../../../README.md)
