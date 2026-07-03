# ANSWER 13 7

**Question 7**

**Which command restores a dropped table during the retention period?**

**A. RESTORE TABLE** ❌ Incorrect

- RESTORE is used with Delta Lake to restore a table to an earlier version.

- It does **not** recover a dropped table.

**B. RECOVER TABLE** ❌ Incorrect

- No such SQL command exists.

**C. UNDROP TABLE** ✅ Correct

Example:

UNDROP TABLE sales;

Requirements:

- Table must still be within the retention period.

- Recovery window must not have expired.

**D. CREATE TABLE RESTORE** ❌ Incorrect

- Invalid SQL syntax.

**E. RELOAD TABLE** ❌ Incorrect

- Reloading and recovering are different operations.

**Memory Trick**

Dropped?

↓

Think:

UNDO

------------------------------------------------------------------------

# [README](./../../../README.md)
