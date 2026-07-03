# ANSWER 15 9

**Question 9**

**After adding the IS_ACTIVE column, why can INSERT \* no longer be used during the MERGE operation?**

**A. MERGE does not support INSERT after UPDATE.** ❌ Incorrect

- MERGE supports both.

**B. Delta Lake disables wildcard inserts after schema changes.** ❌ Incorrect

- Wildcard inserts are allowed when schemas match.

**C. The source and target schemas no longer match, requiring explicit column mappings.** ✅ Correct

Originally:

Source:

EMP_ID\
NAME\
SALARY

Target:

EMP_ID\
NAME\
SALARY\
IS_ACTIVE

Now:

INSERT \*

doesn't know what value belongs in IS_ACTIVE.

Instead:

INSERT\
(\
EMP_ID,\
NAME,\
SALARY,\
IS_ACTIVE\
)\
\
VALUES\
(\
source.EMP_ID,\
source.NAME,\
source.SALARY,\
TRUE\
)

**D. INSERT \* works only for external tables.** ❌ Incorrect

- It works for both table types when schemas match.

**E. The table must first be optimized.** ❌ Incorrect

- Optimization has nothing to do with schema matching.

**Memory Trick**

Schemas Different?

↓

Explicit Mapping Required

------------------------------------------------------------------------

# [README](./../../../README.md)
