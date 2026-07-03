# ANSWER 09 4

**Question 4**

**Which statement correctly describes a managed table in the Hive Metastore?**

**A. The user must always specify the storage location.** ❌ Incorrect

- This describes an **external table**.

Managed tables choose the storage location automatically.

**B. Databricks manages both the table metadata and the physical data files.** ✅ Correct

For managed tables Databricks controls:

- Metadata

- Storage location

- Physical files

- Cleanup when dropped

Everything is managed for you.

**C. Only metadata is managed by Databricks.** ❌ Incorrect

- Physical files are also managed.

**D. Data is always stored in Azure Blob Storage chosen by the user.** ❌ Incorrect

- The user does not choose the location for managed tables.

**E. Managed tables cannot use Delta Lake.** ❌ Incorrect

- Managed tables commonly use Delta Lake.

Example:

CREATE TABLE sales\
USING DELTA

**Memory Trick**

Managed Table = Databricks manages **everything**

------------------------------------------------------------------------

# [README](./../../../README.md)
