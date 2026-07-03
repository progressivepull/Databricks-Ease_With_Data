# ANSWER 16 1

**Question 1**

**What is the primary purpose of Deletion Vectors in Delta Lake?**

**A. To compress Parquet files automatically** ❌ Incorrect

- Compression is handled by the Parquet format itself (such as Snappy, Gzip, or ZSTD).

- Deletion Vectors are about **tracking deleted rows**, not compressing data.

**B. To avoid rewriting entire Parquet files when rows are deleted** ✅ Correct

Before Deletion Vectors:

Suppose a Parquet file contains:

File A\
--------\
1 Alice\
2 Bob\
3 Carol\
4 David

Delete Bob:

DELETE FROM employees\
WHERE id = 2;

Without Deletion Vectors:

Read File A\
↓\
\
Create New File\
\
1 Alice\
3 Carol\
4 David\
\
↓\
\
Delete Old File

This is expensive because the entire file must be rewritten.

With Deletion Vectors:

Original File\
------------\
1 Alice\
2 Bob\
3 Carol\
4 David\
\
Deletion Vector\
\
ID 2 = Deleted

The Parquet file stays unchanged.

Queries simply skip Bob.

This makes DELETE operations much faster.

**C. To create Delta table backups** ❌ Incorrect

- Deletion Vectors do not create backups.

- Time Travel and cloning are used for recovery.

**D. To partition tables by date** ❌ Incorrect

- Partitioning organizes data into folders.

- Deletion Vectors manage deleted rows.

**E. To replace the OPTIMIZE command** ❌ Incorrect

- OPTIMIZE is still used.

- In fact, OPTIMIZE often works together with Deletion Vectors.

**Key Concept**

Without Deletion Vectors

DELETE\
\
↓\
\
Rewrite Entire File

With Deletion Vectors

DELETE\
\
↓\
\
Mark Row Deleted

# [README](./../../../README.md)
