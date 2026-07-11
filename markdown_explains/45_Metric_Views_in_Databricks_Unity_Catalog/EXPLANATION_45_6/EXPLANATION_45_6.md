# EXPLANATION 45 6

**Question 6**

**Which SQL statement is not supported when querying a Metric View?**

**Correct Answer:**\
**C. SELECT \* FROM orders_metric_view**

**Why C is Correct**

Metric Views are **not** queried like ordinary SQL views.

Instead of selecting every column with:

SELECT \*

FROM orders_metric_view;

you query dimensions and measures explicitly, using the semantic model.

This preserves governed business logic and avoids ambiguous access to raw fields.

**Why the other choices are wrong**

Supported queries explicitly reference measures and dimensions rather than using SELECT \*.

**Memory Tip**

**Metric Views ≠ Regular SQL Views**

**Individual YouTube Video**

https://www.youtube.com/watch?v=qhNohS4Lj24

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Metric+View+query

------------------------------------------------------------------------

# [README](./../../../README.md)
