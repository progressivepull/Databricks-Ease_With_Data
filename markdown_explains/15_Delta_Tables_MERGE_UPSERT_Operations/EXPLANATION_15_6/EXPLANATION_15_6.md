# EXPLANATION 15 6

**Question 6**

**Which MERGE clause handles records that exist in the target table but no longer exist in the source table?**

**Correct Answer:**\
✅ **WHEN NOT MATCHED BY SOURCE**

**Explanation**

Example:

Source

1001\
\
1002

Target

1001\
\
1002\
\
1003

Employee 1003 disappeared.

MERGE executes:

WHEN NOT MATCHED BY SOURCE

Possible actions:

DELETE

or

UPDATE SET IS_ACTIVE = FALSE

This is commonly used to synchronize target data with the latest source data. Databricks supports WHEN NOT MATCHED BY SOURCE for these scenarios.

**Flow**

Target Only\
\
↓\
\
WHEN NOT MATCHED BY SOURCE\
\
↓\
\
DELETE\
\
or\
\
Soft Delete

**YouTube**

**MERGE DELETE Example**

https://www.youtube.com/results?search_query=Databricks+MERGE+DELETE

# [README](./../../../README.md)
