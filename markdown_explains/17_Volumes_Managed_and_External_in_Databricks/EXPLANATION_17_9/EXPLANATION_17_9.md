# EXPLANATION 17 9

**Question 9**

**What happens when a Managed Volume is dropped?**

**Correct Answer:**\
✅ **Both the metadata and stored files are permanently deleted.**

**Explanation**

Managed Volumes behave like Managed Tables.

Example:

Managed Volume\
\
↓\
\
DROP VOLUME\
\
↓\
\
Metadata Deleted\
\
↓\
\
Files Deleted

Since Unity Catalog owns the storage, it removes both:

- Metadata

- Physical files

Be cautious—this permanently deletes the managed files.

**YouTube**

**Managed Volumes**

https://www.youtube.com/results?search_query=Unity+Catalog+Managed+Volume

# [README](./../../../README.md)
