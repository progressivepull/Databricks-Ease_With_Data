# ANSWER 13 6

**Question 6**

**Which SQL command lists recently dropped tables that are still eligible for recovery?**

**A. SHOW TABLES HISTORY** ❌ Incorrect

- No such SQL command exists.

**B. SHOW DROPPED OBJECTS** ❌ Incorrect

- This is not valid SQL.

**C. SHOW TABLES DROPPED IN schema_name** ✅ Correct

Example:

SHOW TABLES DROPPED IN sales;

It lists:

- Dropped tables

- Recovery eligibility

- Drop information

This allows administrators to identify recoverable tables.

**D. LIST RECOVERABLE TABLES** ❌ Incorrect

- Not a Databricks SQL command.

**E. DESCRIBE DROPPED TABLES** ❌ Incorrect

- Also not valid.

**Memory Trick**

Need to find dropped tables?

↓

Use

SHOW TABLES DROPPED IN schema_name;

------------------------------------------------------------------------

# [README](./../../../README.md)
