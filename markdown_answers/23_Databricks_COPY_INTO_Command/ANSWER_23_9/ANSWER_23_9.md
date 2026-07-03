# ANSWER 23 9

**Question 9**

**Which feature of COPY INTO allows loading data into a table whose schema changes over time?**

**A. Delta Cloning** ❌ Incorrect

- Cloning copies tables.

**B. Schema Evolution** ✅ Correct

Example:

Original file:

ID\
\
Name

Later file:

ID\
\
Name\
\
Department

Schema Evolution allows the table to grow by adding the new column instead of failing because the schema changed.

**C. Photon Execution** ❌ Incorrect

- Photon improves performance.

**D. Liquid Clustering** ❌ Incorrect

- Clustering improves data organization.

**E. Auto Scaling** ❌ Incorrect

- Auto Scaling adjusts compute resources.

**Memory Trick**

Schema Changes

↓

Schema Evolution

# [README](./../../../README.md)
