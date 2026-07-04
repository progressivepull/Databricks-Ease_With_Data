# EXPLANATION 09 8

**Question 8**

**What happens when an external table is dropped?**

**Correct Answer:**\
✅ **Only the metadata is removed while the data files remain.**

**Explanation**

External tables point to customer-owned storage.

When dropped:

Metadata:

❌ Deleted

Files:

✅ Remain

Example:

ADLS\
\
sales.parquet\
\
customers.parquet

After:

DROP TABLE sales;

The files still exist.

This allows the table to be recreated later.

**YouTube**

**External Tables in Databricks**

https://www.youtube.com/results?search_query=Databricks+External+Tables

# [README](./../../../README.md)
