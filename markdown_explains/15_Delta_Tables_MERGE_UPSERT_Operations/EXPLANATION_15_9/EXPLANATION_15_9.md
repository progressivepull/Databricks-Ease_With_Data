# EXPLANATION 15 9

**Question 9**

**After adding the IS_ACTIVE column, why can INSERT \* no longer be used during the MERGE operation?**

**Correct Answer:**\
✅ **The source and target schemas no longer match, requiring explicit column mappings.**

**Explanation**

Originally:

Source

EMP_ID\
\
NAME\
\
SALARY

Target

EMP_ID\
\
NAME\
\
SALARY

Schemas matched.

After adding:

IS_ACTIVE

Target becomes:

EMP_ID\
\
NAME\
\
SALARY\
\
IS_ACTIVE

Now:

INSERT \*

doesn't know what value should be inserted into IS_ACTIVE.

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

Explicit column mapping solves the schema mismatch.

**YouTube**

**Delta MERGE Column Mapping**

https://www.youtube.com/results?search_query=Delta+Lake+MERGE+Column+Mapping

# [README](./../../../README.md)
