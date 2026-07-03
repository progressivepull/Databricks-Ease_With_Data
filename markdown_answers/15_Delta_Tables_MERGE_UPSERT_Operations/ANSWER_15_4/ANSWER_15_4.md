# ANSWER 15 4

**Question 4**

**Which MERGE clause is executed when matching records are found in both the source and target tables?**

**A. WHEN INSERTED** ❌ Incorrect

- No such MERGE clause exists.

**B. WHEN FOUND** ❌ Incorrect

- Invalid syntax.

**C. WHEN MATCHED** ✅ Correct

Example:

WHEN MATCHED THEN\
UPDATE SET ...

This executes whenever:

Source\
\
↓\
\
EMP_ID = 1001\
\
↓\
\
Target also has EMP_ID = 1001

The existing row is updated.

**D. WHEN UPDATED** ❌ Incorrect

- Not valid syntax.

**E. WHEN EXISTS** ❌ Incorrect

- Also invalid.

**Memory Trick**

Rows match?

↓

WHEN MATCHED

------------------------------------------------------------------------

# [README](./../../../README.md)
