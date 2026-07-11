# EXPLANATION 27 6

**Question 6**

**How does Delta Live Tables handle schema evolution when a developer renames a column or adds a new aggregation?**

**Correct Answer:** **C. Only the transformation code needs to be updated, and DLT automatically applies the schema changes during execution.**

**Explanation**

Developers update the transformation logic. During the next pipeline update, DLT detects the schema changes and updates the managed datasets accordingly.

**Why the Correct Answer is Correct**

DLT manages the underlying table definitions and metadata automatically, reducing manual schema management.

**Why the Other Answers Are Wrong**

They suggest manually recreating tables or editing metadata, which is generally unnecessary.

**YouTube Video**\
<https://www.youtube.com/watch?v=iqf_QHC7tgQ>

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=iqf_QHC7tgQ>

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+DLT+schema+evolution

------------------------------------------------------------------------

# [README](./../../../README.md)
