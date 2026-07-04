# EXPLANATION 13 7

**Question 7**

**Which command restores a dropped table during the retention period?**

**Correct Answer:**\
✅ **UNDROP TABLE**

**Explanation**

Example:

UNDROP TABLE sales;

If the table is still within the retention period:

Dropped Table\
\
↓\
\
UNDROP\
\
↓\
\
Restored

If the retention period has expired, recovery is no longer possible.

This feature is unique to Unity Catalog managed tables and is one of its major improvements over the legacy Hive Metastore.

**YouTube**

**Unity Catalog UNDROP TABLE**

https://www.youtube.com/results?search_query=Unity+Catalog+UNDROP+TABLE

# [README](./../../../README.md)
