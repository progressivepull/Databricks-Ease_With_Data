# EXPLANATION 13 8

**Question 8**

**For how long does Unity Catalog retain dropped managed tables so they can be recovered?**

**Correct Answer:**\
✅ **7 days**

**Explanation**

Timeline:

Day 0\
\
DROP TABLE\
\
↓\
\
Days 1–7\
\
UNDROP Allowed\
\
↓\
\
After Day 7\
\
Permanent Deletion

This recovery period gives administrators time to recover tables that were accidentally deleted.

**Memory Trick**

Unity Catalog Recovery

↓

**7 Days**

**YouTube**

**Unity Catalog Recovery Features**

https://www.youtube.com/results?search_query=Unity+Catalog+Recovery

# [README](./../../../README.md)
