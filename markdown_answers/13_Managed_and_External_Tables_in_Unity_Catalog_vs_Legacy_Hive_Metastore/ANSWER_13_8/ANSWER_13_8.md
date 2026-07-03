# ANSWER 13 8

**Question 8**

**For how long does Unity Catalog retain dropped managed tables so they can be recovered?**

**A. 24 hours** ❌ Incorrect

- Too short.

**B. 3 days** ❌ Incorrect

- Not the default.

**C. 5 days** ❌ Incorrect

- Also incorrect.

**D. 7 days** ✅ Correct

Unity Catalog keeps dropped managed tables for **7 days** by default.

Timeline:

Day 0\
DROP TABLE\
\
↓\
\
Days 1-7\
UNDROP allowed\
\
↓\
\
After Day 7\
Permanent deletion

**E. 30 days** ❌ Incorrect

- Longer than the default retention period.

**Memory Trick**

Unity Catalog Recovery

↓

**7 Days**

------------------------------------------------------------------------

# [README](./../../../README.md)
