# ANSWER 17 9

**Question 9**

**What happens when a Managed Volume is dropped?**

**A. Only the metadata is removed.** ❌ Incorrect

- This behavior belongs to External Volumes.

**B. Only the files are removed.** ❌ Incorrect

- Metadata is also removed.

**C. Both the metadata and stored files are permanently deleted.** ✅ Correct

Managed Volume:

DROP VOLUME\
\
↓\
\
Metadata Deleted\
\
+\
\
Files Deleted

This mirrors the behavior of managed tables.

**D. The volume is converted into an External Volume.** ❌ Incorrect

- Object type never changes automatically.

**E. The files are archived automatically.** ❌ Incorrect

- There is no automatic archive.

------------------------------------------------------------------------

**Memory Trick**

Managed

↓

Unity Catalog owns everything.

Drop

↓

Everything deleted.

------------------------------------------------------------------------

# [README](./../../../README.md)
