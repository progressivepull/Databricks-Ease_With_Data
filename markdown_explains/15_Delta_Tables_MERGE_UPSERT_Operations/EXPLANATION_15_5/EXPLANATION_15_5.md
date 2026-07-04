# EXPLANATION 15 5

**Question 5**

**Which MERGE clause inserts records that exist in the source table but not in the target table?**

**Correct Answer:**\
✅ **WHEN NOT MATCHED**

**Explanation**

Example:

Target

1001\
\
1002

Source

1001\
\
1002\
\
1003

Employee 1003 doesn't exist.

MERGE executes:

WHEN NOT MATCHED THEN\
INSERT (...)

**Flow**

Not Found\
\
↓\
\
INSERT

**YouTube**

**MERGE INSERT Example**

https://www.youtube.com/results?search_query=Databricks+MERGE+INSERT

# [README](./../../../README.md)
