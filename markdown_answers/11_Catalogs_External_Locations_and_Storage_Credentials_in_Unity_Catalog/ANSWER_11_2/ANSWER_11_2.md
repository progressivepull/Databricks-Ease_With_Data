# ANSWER 11 2

**Question 2**

**If neither a schema nor a catalog has a managed location configured, where will managed table data be stored?**

**A. Azure Blob root container** ❌ Incorrect

- Unity Catalog does not automatically use the root of a storage account.

- It uses the managed storage configured for the metastore.

**B. External Location** ❌ Incorrect

- External Locations are only used for external tables.

**C. Local DBFS only** ❌ Incorrect

- Unity Catalog does not rely on DBFS for managed table storage.

- Managed storage is cloud object storage.

**D. Metastore Managed Location** ✅ Correct

If:

- Schema has no managed location

- Catalog has no managed location

Unity Catalog stores the table here:

Metastore Managed Location

This is the default storage location.

**E. Temporary workspace storage** ❌ Incorrect

- Temporary workspace storage is unrelated to Unity Catalog managed tables.

**Memory Trick**

No Schema Location?

↓

No Catalog Location?

↓

Use Metastore Location

# [README](./../../../README.md)
