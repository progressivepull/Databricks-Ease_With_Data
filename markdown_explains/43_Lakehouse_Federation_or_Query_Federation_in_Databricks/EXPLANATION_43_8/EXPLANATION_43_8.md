# EXPLANATION 43 8

**Question 8**

**How does Databricks query data in a Foreign Catalog?**

**Correct Answer:**\
**C. It uses the same SQL syntax as native Unity Catalog tables while reading data from the external database.**

**Why C is Correct**

One of the biggest advantages of Lakehouse Federation is transparency.

Users simply write:

SELECT \*

FROM foreign_catalog.sales.orders;

The SQL syntax is the same as querying native Unity Catalog tables, while Databricks pushes supported operations down to the external database whenever possible.

**Why the other choices are wrong**

You do not need a different SQL language or special syntax.

**Memory Tip**

**Same SQL, Different Storage**

**Individual YouTube Video**

https://www.youtube.com/watch?v=mdw5j0l7K2Y

**YouTube Search**

https://www.youtube.com/results?search_query=Query+Foreign+Catalog+Databricks

------------------------------------------------------------------------

# [README](./../../../README.md)
