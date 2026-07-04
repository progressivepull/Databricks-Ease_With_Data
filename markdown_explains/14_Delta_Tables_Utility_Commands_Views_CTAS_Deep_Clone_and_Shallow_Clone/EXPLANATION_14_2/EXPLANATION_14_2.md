# EXPLANATION 14 2

**Question 2**

**Which PySpark command checks whether a table exists?**

**Correct Answer:**\
✅ **spark.catalog.tableExists()**

**Explanation**

PySpark includes a **Catalog API** that lets you inspect objects stored in the metastore.

Example:

spark.catalog.tableExists(\
"finance.sales.orders"\
)

Returns:

True

or

False

This is useful before creating or querying a table.

Example:

if spark.catalog.tableExists("finance.sales.orders"):\
print("Table exists")\
else:\
print("Create table")

**Why use it?**

It prevents errors such as:

Table Already Exists\
\
or\
\
Table Not Found

**YouTube**

**PySpark Catalog API**

https://www.youtube.com/results?search_query=PySpark+Catalog+tableExists

# [README](./../../../README.md)
