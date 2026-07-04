# EXPLANATION 15 4

**Question 4**

**Which MERGE clause is executed when matching records are found in both the source and target tables?**

**Correct Answer:**\
✅ **WHEN MATCHED**

**Explanation**

If:

Source EMP_ID = 1001\
\
Target EMP_ID = 1001

MERGE executes:

WHEN MATCHED\
THEN UPDATE ...

Typical use:

WHEN MATCHED THEN\
UPDATE SET\
salary = source.salary

**Workflow**

Match Found\
\
↓\
\
WHEN MATCHED\
\
↓\
\
UPDATE

**YouTube**

**MERGE WHEN MATCHED**

https://www.youtube.com/results?search_query=Databricks+MERGE+WHEN+MATCHED

# [README](./../../../README.md)
