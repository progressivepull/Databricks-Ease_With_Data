# EXPLANATION 45 5

**Question 5**

**How are reusable measures referenced when querying a Metric View?**

**Correct Answer:**\
**C. measure(total_orders)**

**Why C is Correct**

Metric Views expose reusable measures using the measure() function.

Example:

SELECT

measure(total_orders)

FROM orders_metrics;

This tells Databricks to use the centrally defined business logic for total_orders instead of rewriting the calculation in every query.

**Why the other choices are wrong**

The lesson specifically demonstrates the measure() syntax for reusable metrics.

**Memory Tip**

**Reusable KPI = measure()**

**Individual YouTube Video**

https://www.youtube.com/watch?v=75zcOOk6How

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+measure()+Metric+Views

------------------------------------------------------------------------

# [README](./../../../README.md)
