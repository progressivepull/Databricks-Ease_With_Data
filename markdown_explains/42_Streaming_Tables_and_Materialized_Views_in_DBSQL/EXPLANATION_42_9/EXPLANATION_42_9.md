# EXPLANATION 42 9

**Question 9**

**What optimization does Databricks perform when a Materialized View refresh detects no new data?**

**Correct Answer:**\
**C. It performs a No Operation (NO OP), skipping unnecessary processing.**

**Why C is Correct**

During refresh, Databricks checks whether the source data has changed.

If no changes are detected:

- No recomputation occurs.

- Compute resources are not wasted.

- Existing results remain valid.

This optimization is commonly referred to as a **NO OP (No Operation)** refresh.

**Why the other choices are wrong**

Databricks does not reload all data or rebuild the Materialized View when nothing has changed.

**Memory Tip**

**No Changes = No Work**

**Individual YouTube Video**

Materialized View Incremental Refresh

https://www.youtube.com/watch?v=WWM4Y8R7n8Q

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Materialized+View+refresh

------------------------------------------------------------------------

# [README](./../../../README.md)
