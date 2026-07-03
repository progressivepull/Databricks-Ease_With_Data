# ANSWER 15 5

**Question 5**

**Which MERGE clause inserts records that exist in the source table but not in the target table?**

**A. WHEN MATCHED** ❌ Incorrect

- Used for updates.

**B. WHEN INSERTED** ❌ Incorrect

- Invalid syntax.

**C. WHEN NOT MATCHED** ✅ Correct

Example:

Target:

1001\
1002

Source:

1001\
1002\
1003

Employee 1003 doesn't exist.

MERGE executes:

WHEN NOT MATCHED THEN\
INSERT (...)

**D. WHEN NEW RECORD** ❌ Incorrect

- Not valid SQL.

**E. WHEN SOURCE EXISTS** ❌ Incorrect

- Also invalid.

**Memory Trick**

Not found?

↓

Insert.

------------------------------------------------------------------------

# [README](./../../../README.md)
