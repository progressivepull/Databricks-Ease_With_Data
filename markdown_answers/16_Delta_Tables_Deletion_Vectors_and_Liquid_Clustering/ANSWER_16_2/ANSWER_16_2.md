# ANSWER 16 2

**Question 2**

**How are deleted rows handled when Deletion Vectors are enabled?**

**A. They are immediately removed from the Parquet file.** ❌ Incorrect

- This is how Delta Lake traditionally worked.

- Deletion Vectors avoid immediate rewrites.

**B. They are copied into a new Delta table.** ❌ Incorrect

- No new table is created.

**C. They are marked as deleted, and queries ignore them until physical cleanup occurs.** ✅ Correct

Think of a sticky note placed on the row:

Alice\
\
Bob ← Deleted\
\
Carol\
\
David

The row still exists physically.

Queries behave as though it doesn't exist.

Later, physical cleanup removes it.

**D. They are moved into the Hive Metastore.** ❌ Incorrect

- Hive Metastore stores metadata, not deleted rows.

**E. They are converted into NULL values.** ❌ Incorrect

- The row is hidden, not modified.

**Memory Trick**

Deletion Vector

↓

Invisible

Not Removed

# [README](./../../../README.md)
