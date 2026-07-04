# EXPLANATION 17 4

**Question 4**

**Which statement correctly describes a Managed Volume?**

**Correct Answer:**\
✅ **Unity Catalog automatically determines where files are stored.**

**Explanation**

A Managed Volume works much like a Managed Table.

When you create it:

CREATE VOLUME images;

Unity Catalog chooses the storage location automatically.

You do **not** specify:

LOCATION ...

Unity Catalog stores the files in managed storage.

**Comparison**

Managed Volume

Unity Catalog\
\
↓\
\
Chooses Storage

External Volume

User\
\
↓\
\
Chooses Storage

**YouTube**

**Managed vs External Volumes**

https://www.youtube.com/results?search_query=Unity+Catalog+Managed+Volume

# [README](./../../../README.md)
