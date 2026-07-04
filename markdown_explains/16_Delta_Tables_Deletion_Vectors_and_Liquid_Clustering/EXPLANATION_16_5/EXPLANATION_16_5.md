# EXPLANATION 16 5

**Question 5**

**What information can be observed in DESCRIBE HISTORY after performing DELETE operations?**

**Correct Answer:**\
✅ **Operation metrics such as files rewritten and deletion vectors added**

**Explanation**

Example:

DESCRIBE HISTORY employees;

The output includes information such as:

- Operation type

- Timestamp

- User

- Number of rows affected

- Files Added

- Files Removed

- Operation Metrics

When Deletion Vectors are used, the operation metrics indicate how the operation was performed, including whether deletion vectors were written instead of rewriting entire files.

**Example**

DELETE\
\
Rows Deleted\
\
Files Rewritten\
\
Deletion Vectors Added

**YouTube**

**DESCRIBE HISTORY Delta Lake**

https://www.youtube.com/results?search_query=Databricks+DESCRIBE+HISTORY

# [README](./../../../README.md)
