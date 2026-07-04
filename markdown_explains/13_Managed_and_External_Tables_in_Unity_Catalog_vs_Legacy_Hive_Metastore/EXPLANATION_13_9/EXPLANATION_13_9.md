# EXPLANATION 13 9

**Question 9**

**When an external table is dropped in Unity Catalog, what happens to the physical data files?**

**Correct Answer:**\
✅ **They are retained permanently in the external storage location.**

**Explanation**

External tables separate metadata from data.

Example:

Azure Storage\
\
sales.parquet\
\
customers.parquet

After:

DROP TABLE sales;

Result:

Metadata:

❌ Removed

Files:

✅ Remain

The files are untouched because they belong to the customer.

The table can later be recreated by pointing to the same storage location.

**YouTube**

**External Tables in Unity Catalog**

https://www.youtube.com/results?search_query=Unity+Catalog+External+Tables

# [README](./../../../README.md)
