# EXPLANATION 09 9

**Question 9**

**Why can an external table be recreated after it has been dropped?**

**Correct Answer:**\
✅ **The physical data remains in the specified external storage location.**

**Explanation**

Only the metadata is removed.

The files stay in storage.

Example:

ADLS\
\
orders.delta

Drop table:

DROP TABLE orders;

Result:

Metadata\
\
↓\
\
Deleted\
\
Files\
\
↓\
\
Remain

You can recreate the table by pointing to the same storage location.

This separation between metadata and data is the key advantage of external tables.

**YouTube**

**External Tables Tutorial**

https://www.youtube.com/results?search_query=Databricks+External+Tables+Tutorial

# [README](./../../../README.md)
