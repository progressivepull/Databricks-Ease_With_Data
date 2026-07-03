# ANSWER 14 10

**Question 10**

**Which operation can negatively impact a Shallow Clone because it initially references the original table's data files?**

**A. OPTIMIZE** ❌ Incorrect

- OPTIMIZE reorganizes data files for performance.

- It does not normally invalidate a shallow clone.

**B. MERGE** ❌ Incorrect

- MERGE updates table contents but is not the primary risk highlighted here.

**C. DESCRIBE HISTORY** ❌ Incorrect

- This command is read-only.

- It never affects data.

**D. VACUUM** ✅ Correct

VACUUM removes old, unreferenced data files.

A shallow clone initially depends on the original table's files.

Example:

Original Table\
\
↓\
\
Data Files\
\
↑\
\
Shallow Clone

If the source table is vacuumed and required files are permanently removed, the shallow clone may no longer be able to access those files correctly.

This is why shallow clones require careful management when VACUUM is used.

**E. CREATE VIEW** ❌ Incorrect

- Views have no effect on the underlying data files.

**Memory Trick**

Shallow Clone

↓

Shares Files

↓

VACUUM

↓

May remove shared files

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| List catalogs | SHOW CATALOGS; |
| Check if a table exists (PySpark) | spark.catalog.tableExists() |
| Safe table creation | CREATE TABLE IF NOT EXISTS prevents errors if the table already exists |
| Delta transaction history | DESCRIBE HISTORY table_name; |
| Temporary view | Exists only for the current Spark session |
| Permanent view | Persists in the metastore after clusters restart |
| CTAS | Creates a new table by copying data, but may not preserve all metadata |
| Deep Clone | Creates a complete, independent copy including data and metadata |
| Shallow Clone | Copies metadata and initially references the source table's data files |
| Risk to Shallow Clone | VACUUM can remove source data files that the shallow clone still references |

# [README](./../../../README.md)
