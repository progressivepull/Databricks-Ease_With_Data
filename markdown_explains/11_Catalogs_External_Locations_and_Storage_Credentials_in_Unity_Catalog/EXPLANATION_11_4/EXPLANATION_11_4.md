# EXPLANATION 11 4

**Question 4**

**Which schemas are automatically created when a new catalog is created?**

**Correct Answer:**\
✅ **default and information_schema**

**Explanation**

Every new catalog automatically contains two schemas:

**1. default**

Used for general user objects.

Example:

CREATE TABLE default.sales (...)

**2. information_schema**

Contains metadata about the catalog.

Examples include:

- Tables

- Columns

- Views

- Privileges

- Schemas

Example query:

SELECT \*\
\
FROM information_schema.tables;

This allows administrators and developers to inspect metadata using standard SQL.

**YouTube**

**Unity Catalog Schemas**

https://www.youtube.com/results?search_query=Unity+Catalog+Schemas

------------------------------------------------------------------------

# [README](./../../../README.md)
