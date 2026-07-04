# EXPLANATION 16 2

**Question 2**

**How are deleted rows handled when Deletion Vectors are enabled?**

**Correct Answer:**\
✅ **They are marked as deleted, and queries ignore them until physical cleanup occurs.**

**Explanation**

Deletion Vectors perform a **logical delete**, not an immediate physical delete.

Example:

Alice\
\
Bob\
\
Carol

Delete Bob:

Alice\
\
Bob ← Marked Deleted\
\
Carol

The row still exists physically inside the Parquet file.

When queries run:

SELECT \*\
FROM employees;

they behave as if Bob never existed.

Eventually, maintenance operations rewrite the files and physically remove the deleted rows. Databricks documentation describes this as applying deletion vector metadata during reads until data files are rewritten.

**YouTube**

**Deletion Vectors Explained**

https://www.youtube.com/results?search_query=Delta+Lake+Deletion+Vectors

# [README](./../../../README.md)
