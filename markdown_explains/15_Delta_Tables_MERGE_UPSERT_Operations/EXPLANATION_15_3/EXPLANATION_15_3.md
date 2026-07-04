# EXPLANATION 15 3

**Question 3**

**In the lesson's MERGE example, which column is used as the business key to compare the source and target tables?**

**Correct Answer:**\
✅ **EMP_ID**

**Explanation**

A **business key** uniquely identifies a record.

Example:

EMP_ID\
\
1001\
\
1002\
\
1003

MERGE compares:

ON target.EMP_ID = source.EMP_ID

Everything else may change:

- Name

- Salary

- Department

but **EMP_ID** identifies the employee.

**Why not Name?**

Names change.

Example:

John Smith\
\
↓\
\
John Johnson

Employee ID does not.

**YouTube**

**Business Keys in Delta MERGE**

https://www.youtube.com/results?search_query=Delta+Lake+Business+Key

# [README](./../../../README.md)
