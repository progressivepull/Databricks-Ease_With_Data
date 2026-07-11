# EXPLANATION 42 8

**Question 8**

**Why do Materialized Views improve dashboard and reporting performance?**

**Correct Answer:**\
**C. They store precomputed query results instead of recomputing expensive aggregations each time.**

**Why C is Correct**

Business dashboards often execute complex SQL with joins and aggregations.

Materialized Views cache those results, so dashboards read the stored output instead of recomputing it on every request.

Benefits include:

- Faster dashboards

- Lower latency

- Reduced compute usage

**Why the other choices are wrong**

Materialized Views do not make SQL faster by changing SQL syntax or increasing CPU resources; they improve performance by reusing stored results.

**Memory Tip**

**Materialized View = Cached Analytics**

**Individual YouTube Video**

Materialized Views Overview

https://www.youtube.com/watch?v=WWM4Y8R7n8Q

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Materialized+Views+performance

------------------------------------------------------------------------

# [README](./../../../README.md)
