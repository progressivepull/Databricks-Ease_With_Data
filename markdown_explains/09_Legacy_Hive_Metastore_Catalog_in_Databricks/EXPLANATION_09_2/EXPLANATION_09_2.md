# EXPLANATION 09 2

**Question 2**

**Which namespace format is used by the Hive Metastore?**

**Correct Answer:**\
✅ **schema.table**

**Explanation**

Hive Metastore uses a **two-level namespace**.

Example:

sales.orders

Where:

sales\
\
↓\
\
Schema\
\
orders\
\
↓\
\
Table

Unlike Unity Catalog, there is **no catalog level**.

**Comparison**

Hive Metastore

schema.table

Unity Catalog

catalog.schema.table

Adding the catalog level allows Unity Catalog to support multiple catalogs within a single metastore.

**YouTube**

**Unity Catalog Three-Level Namespace**

https://www.youtube.com/results?search_query=Unity+Catalog+catalog+schema+table

# [README](./../../../README.md)
