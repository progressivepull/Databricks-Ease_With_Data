# EXPLANATION 08 9

**Question 9**

**How are tables referenced in Unity Catalog?**

**Correct Answer:**\
✅ **catalog.schema.table**

**Explanation**

Unity Catalog uses **three-level namespaces**.

Example:

finance.sales.orders

Where:

finance\
\
↓\
\
Catalog\
\
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

This uniquely identifies a table across multiple catalogs.

**Comparison**

Hive Metastore

schema.table

Unity Catalog

catalog.schema.table

**YouTube**

**Unity Catalog Three-Level Namespace**

https://www.youtube.com/results?search_query=Unity+Catalog+catalog+schema+table

# [README](./../../../README.md)
