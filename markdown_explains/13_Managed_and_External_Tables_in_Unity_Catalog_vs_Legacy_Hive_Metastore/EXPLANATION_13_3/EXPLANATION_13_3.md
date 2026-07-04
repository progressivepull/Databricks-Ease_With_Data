# EXPLANATION 13 3

**Question 3**

**Where is the data for a managed table stored when no storage location is specified?**

**Correct Answer:**\
✅ **In Unity Catalog's managed storage location (catalog or metastore managed location)**

**Explanation**

Managed tables use **managed storage**.

Unity Catalog automatically chooses the storage location using this priority:

Schema Managed Location\
↓\
Catalog Managed Location\
↓\
Metastore Managed Location

If no schema or catalog location exists, the metastore location is used.

The user does **not** specify a LOCATION clause.

**YouTube**

**Unity Catalog Managed Storage**

https://www.youtube.com/results?search_query=Unity+Catalog+Managed+Storage

# [README](./../../../README.md)
