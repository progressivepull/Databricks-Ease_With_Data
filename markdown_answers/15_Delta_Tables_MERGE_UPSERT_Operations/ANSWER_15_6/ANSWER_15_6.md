# ANSWER 15 6

**Question 6**

**Which MERGE clause handles records that exist in the target table but no longer exist in the source table?**

**A. WHEN MATCHED BY TARGET** ❌ Incorrect

- Not valid syntax.

**B. WHEN NOT MATCHED BY SOURCE** ✅ Correct

Example:

Source:

1001\
1002

Target:

1001\
1002\
1003

Employee 1003 no longer exists.

MERGE executes:

WHEN NOT MATCHED BY SOURCE

Possible actions:

- DELETE

- UPDATE IS_ACTIVE = FALSE

This is commonly used for synchronization.

**C. WHEN NOT MATCHED BY TARGET** ❌ Incorrect

- Incorrect syntax.

**D. WHEN SOURCE MISSING** ❌ Incorrect

- Invalid.

**E. WHEN DELETE REQUIRED** ❌ Incorrect

- Invalid.

**Memory Trick**

Target only?

↓

Not Matched By Source

------------------------------------------------------------------------

# [README](./../../../README.md)
