# EXPLANATION 13 5

**Question 5**

**How does Unity Catalog handle a managed table after it is dropped?**

**Correct Answer:**\
✅ **Metadata is removed, but data files are temporarily retained for recovery.**

**Explanation**

Unity Catalog adds a safety feature that the legacy Hive Metastore did not have.

When you run:

DROP TABLE sales;

The table enters a recovery period.

DROP TABLE\
\
↓\
\
Metadata Removed\
\
↓\
\
Data Retained\
\
↓\
\
Recovery Possible

During this period, you can recover the table with:

UNDROP TABLE sales;

This helps protect against accidental deletions.

**YouTube**

**Unity Catalog Table Recovery**

https://www.youtube.com/results?search_query=Unity+Catalog+UNDROP+TABLE

# [README](./../../../README.md)
