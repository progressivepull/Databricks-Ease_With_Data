# EXPLANATION 16 1

**Question 1**

**What is the primary purpose of Deletion Vectors in Delta Lake?**

**Correct Answer:**\
✅ **To avoid rewriting entire Parquet files when rows are deleted**

**Explanation**

Normally, when you delete even **one row** from a Parquet file, Delta Lake would need to rewrite the **entire file**.

Example:

Parquet File\
\
1 Alice\
2 Bob\
3 Carol\
4 David

Delete Bob.

**Without Deletion Vectors**

Delta Lake must:

Read File\
\
↓\
\
Rewrite File\
\
↓\
\
Delete Old File

This is expensive because large Parquet files (often 128 MB–1 GB) must be rewritten.

**With Deletion Vectors**

Instead of rewriting the file:

Original File\
\
1 Alice\
2 Bob\
3 Carol\
4 David\
\
↓\
\
Deletion Vector\
\
Row 2 = Deleted

The original Parquet file remains unchanged. Queries use the Deletion Vector metadata to ignore the deleted row, making DELETE, UPDATE, and MERGE operations much faster.

**Memory Trick**

Without DV\
\
DELETE\
\
↓\
\
Rewrite File\
\
----------------\
\
With DV\
\
DELETE\
\
↓\
\
Mark Row Deleted

**YouTube**

**Deletion Vectors in Databricks**

https://www.youtube.com/results?search_query=Databricks+Deletion+Vectors

# [README](./../../../README.md)
