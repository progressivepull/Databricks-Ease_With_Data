# ANSWER 16 3

**Question 3**

**Which command is commonly used to physically remove rows that were marked by Deletion Vectors?**

**A. VACUUM table_name;** ❌ Incorrect

Many learners confuse this.

VACUUM removes:

- old files

- obsolete files

It **does not rewrite files** to eliminate rows marked by Deletion Vectors.

**B. MERGE table_name;** ❌ Incorrect

- MERGE synchronizes data.

- It doesn't clean deletion vectors.

**C. OPTIMIZE table_name;** ✅ Correct

OPTIMIZE rewrites files.

When it rewrites them:

- Deleted rows are omitted.

- Smaller optimized files are created.

- Deletion Vectors are no longer needed for those rows.

Example:

OPTIMIZE employees;

**D. CLUSTER BY table_name;** ❌ Incorrect

- Clustering organizes data.

- It doesn't clean deleted rows.

**E. ANALYZE TABLE table_name;** ❌ Incorrect

- ANALYZE gathers statistics.

**Key Concept**

Deletion Vector

↓

Later

↓

OPTIMIZE

↓

New Files Without Deleted Rows

# [README](./../../../README.md)
