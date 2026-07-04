# EXPLANATION 15 7

**Question 7**

**What is the primary difference between a hard delete and a soft delete?**

**Correct Answer:**\
✅ **Hard delete permanently removes records, while soft delete marks them inactive and preserves history.**

**Explanation**

**Hard Delete**

DELETE\
\
↓\
\
Gone Forever

**Soft Delete**

IS_ACTIVE = FALSE

The row still exists.

Example:

| **EMP_ID** | **Name** | **IS_ACTIVE** |
|------------|----------|---------------|
| 1001       | John     | TRUE          |
| 1002       | Mary     | FALSE         |

Advantages of Soft Delete:

- Auditing

- Historical reporting

- Easier recovery

- Compliance

**YouTube**

**Soft Delete vs Hard Delete**

https://www.youtube.com/results?search_query=Soft+Delete+Hard+Delete+Databricks

# [README](./../../../README.md)
