# EXPLANATION 42 3

**Question 3**

**What is the primary purpose of a Materialized View?**

**Correct Answer:**\
**C. To store precomputed query results for faster analytics**

**Why C is Correct**

Unlike a standard SQL view, a **Materialized View** stores the results of a query physically.

Instead of recalculating expensive joins and aggregations every time:

- Results are computed once.

- Stored on disk.

- Refreshed incrementally.

- Read much faster.

This dramatically improves dashboard performance.

**Why the other choices are wrong**

Materialized Views are not:

- streaming ingestion tables

- storage systems

- security features

- compute engines

**Memory Tip**

**View = Recompute**

**Materialized View = Store Results**

**Individual YouTube Video**

Materialized Views in Databricks

https://www.youtube.com/watch?v=WWM4Y8R7n8Q

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Materialized+Views

------------------------------------------------------------------------

# [README](./../../../README.md)
