# EXPLANATION 27 5

**Question 5**

**What happens to Materialized Views when upstream data changes?**

**Correct Answer:** **C. They automatically recompute joins and aggregations to produce the latest results.**

**Explanation**

Materialized Views automatically refresh whenever upstream datasets change. Databricks determines whether an incremental refresh is possible or whether a full recomputation is required.

**Why the Correct Answer is Correct**

Materialized Views always represent the latest transformed version of the underlying data.

**Why the Other Answers Are Wrong**

The incorrect answers imply manual refreshes or static data.

**YouTube Video**\
<https://www.youtube.com/watch?v=WREJAbBAgv0>

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=WREJAbBAgv0>

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+Materialized+Views+DLT

------------------------------------------------------------------------

# [README](./../../../README.md)
