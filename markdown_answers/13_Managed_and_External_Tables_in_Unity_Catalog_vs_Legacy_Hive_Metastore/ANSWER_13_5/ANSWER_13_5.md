# ANSWER 13 5

**Question 5**

**How does Unity Catalog handle a managed table after it is dropped?**

**A. Both metadata and data are immediately deleted.** ❌ Incorrect

- This was generally true for legacy Hive Metastore managed tables.

- Unity Catalog behaves differently.

**B. Only metadata remains.** ❌ Incorrect

- Metadata is removed.

**C. Metadata is removed, but data files are temporarily retained for recovery.** ✅ Correct

Unity Catalog introduces a recovery feature.

After:

DROP TABLE sales;

The table enters a retention period.

During this period:

- Metadata is marked as dropped.

- Data files remain.

- The table can be recovered.

This enables:

UNDROP TABLE sales;

**D. The table automatically becomes an external table.** ❌ Incorrect

- Table type never changes automatically.

**E. The table is archived permanently.** ❌ Incorrect

- Recovery is temporary, not permanent.

**Key Concept**

Unity Catalog:

DROP TABLE\
\
↓\
\
Recovery Period\
\
↓\
\
Permanent Deletion

------------------------------------------------------------------------

# [README](./../../../README.md)
