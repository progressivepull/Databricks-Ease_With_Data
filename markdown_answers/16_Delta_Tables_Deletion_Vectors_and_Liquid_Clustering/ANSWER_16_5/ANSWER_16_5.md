# ANSWER 16 5

**Question 5**

**What information can be observed in DESCRIBE HISTORY after performing DELETE operations?**

**A. Only the table owner** ❌ Incorrect

- Owner information is available elsewhere.

- DESCRIBE HISTORY contains much more.

**B. Only the storage location** ❌ Incorrect

- Storage location isn't its primary purpose.

**C. Operation metrics such as files rewritten and deletion vectors added** ✅ Correct

Example output includes:

- Operation = DELETE

- Number of rows deleted

- Files added

- Files removed

- Deletion Vectors added

- Execution time

This helps you understand exactly what happened.

**D. Only SQL query history** ❌ Incorrect

- SQL history belongs elsewhere.

**E. Azure subscription information** ❌ Incorrect

- Azure information is unrelated.

**Memory Trick**

DESCRIBE HISTORY

↓

Everything about the transaction

# [README](./../../../README.md)
