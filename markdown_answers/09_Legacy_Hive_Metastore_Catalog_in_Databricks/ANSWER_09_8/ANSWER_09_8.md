# ANSWER 09 8

**Question 8**

**What happens when an external table is dropped?**

**A. Both metadata and data files are deleted.** ❌ Incorrect

- Only managed tables behave this way.

**B. Only the metadata is removed while the data files remain.** ✅ Correct

Databricks forgets where the data is.

The files still exist.

Example:

Cloud Storage\
orders.parquet\
sales.delta

These files remain untouched.

**C. The table is moved to the Hive Metastore default schema.** ❌ Incorrect

- Dropping removes the table definition.

**D. The table becomes read-only.** ❌ Incorrect

- It no longer exists as a table.

**E. The storage location is automatically deleted.** ❌ Incorrect

- External storage belongs to the user.

**Memory Trick**

External Table:

DROP TABLE\
│\
▼\
Metadata deleted\
\
Data stays

------------------------------------------------------------------------

# [README](./../../../README.md)
