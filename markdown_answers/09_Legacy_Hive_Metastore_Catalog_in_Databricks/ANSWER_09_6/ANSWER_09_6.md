# ANSWER 09 6

**Question 6**

**What is the primary difference between a managed table and an external table?**

**A. Managed tables support SQL while external tables do not.** ❌ Incorrect

- Both support SQL.

**B. Managed tables require Unity Catalog, while external tables require Hive Metastore.** ❌ Incorrect

- Both can exist in Hive Metastore and Unity Catalog.

**C. External tables require a user-defined storage location, while managed tables do not.** ✅ Correct

Managed Table:

User creates table\
↓\
Databricks chooses storage

External Table:

User chooses storage location

Example:

LOCATION '/mnt/raw/orders'

The user owns the data location.

**D. Managed tables cannot store structured data.** ❌ Incorrect

- Structured data is exactly what managed tables store.

**E. External tables automatically create views.** ❌ Incorrect

- Tables and views are separate objects.

**Memory Trick**

Managed = Databricks chooses storage

External = You choose storage

------------------------------------------------------------------------

# [README](./../../../README.md)
