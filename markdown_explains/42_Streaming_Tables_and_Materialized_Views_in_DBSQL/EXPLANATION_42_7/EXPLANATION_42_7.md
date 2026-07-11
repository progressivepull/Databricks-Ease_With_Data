# EXPLANATION 42 7

**Question 7**

**Which SQL command performs a full reload of all source data for a Streaming Table?**

**Correct Answer:**\
**C. REFRESH STREAMING TABLE FULL**

**Why C is Correct**

Normally, Streaming Tables process only new data.

REFRESH STREAMING TABLE FULL instructs Databricks to:

- Discard incremental state.

- Re-read all source data.

- Rebuild the Streaming Table completely.

This is useful after major schema changes or when historical data must be reprocessed.

**Why the other choices are wrong**

Other refresh commands perform incremental updates rather than a complete reload.

**Memory Tip**

**FULL = Reload Everything**

**Individual YouTube Video**

Streaming Table Refresh

https://www.youtube.com/watch?v=lR1Q3F2M4qI

**YouTube Search**

https://www.youtube.com/results?search_query=REFRESH+STREAMING+TABLE+FULL+Databricks

------------------------------------------------------------------------

# [README](./../../../README.md)
