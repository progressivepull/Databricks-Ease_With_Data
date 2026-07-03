# ANSWER 14 4

**Question 4**

**Which command displays the transaction history of a Delta table?**

**A. SHOW HISTORY table_name;** ❌ Incorrect

- Not valid Databricks SQL.

**B. HISTORY TABLE table_name;** ❌ Incorrect

- Also not valid syntax.

**C. DESCRIBE HISTORY table_name;** ✅ Correct

Example:

DESCRIBE HISTORY sales.orders;

Shows:

- Version number

- Timestamp

- User

- Operation

- Notebook

- Job

- Cluster

- Operation parameters

This is one of Delta Lake's most valuable auditing features.

**D. LIST HISTORY table_name;** ❌ Incorrect

- No such SQL command.

**E. SHOW VERSIONS table_name;** ❌ Incorrect

- Version information comes from DESCRIBE HISTORY.

**Memory Trick**

Need transaction history?

↓

DESCRIBE HISTORY

# [README](./../../../README.md)
