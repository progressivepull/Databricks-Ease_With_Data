# ANSWER 15 8

**Question 8**

**Which new column is added to support the soft delete implementation in the lesson?**

**A. STATUS_CODE** ❌ Incorrect

- Could be used in some systems but not this lesson.

**B. IS_DELETED** ❌ Incorrect

- Also common but not used here.

**C. ACTIVE_FLAG** ❌ Incorrect

- Similar idea, wrong column name.

**D. IS_ACTIVE** ✅ Correct

Instead of deleting:

Employee\
\
↓\
\
IS_ACTIVE = FALSE

Queries can filter:

WHERE IS_ACTIVE = TRUE

Inactive records remain available for audits.

**E. RECORD_STATUS** ❌ Incorrect

- Not used.

**Memory Trick**

TRUE

↓

Currently Active

FALSE

↓

Soft Deleted

------------------------------------------------------------------------

# [README](./../../../README.md)
