# ANSWER 17 4

**Question 4**

**Which statement correctly describes a Managed Volume?**

**A. It always requires a user-defined storage location.** ❌ Incorrect

- That describes an External Volume.

**B. Unity Catalog automatically determines where files are stored.** ✅ Correct

Managed Volume:

You create Volume\
\
↓\
\
Unity Catalog chooses storage

Exactly like managed tables.

You don't specify a LOCATION.

**C. It stores only unstructured data.** ❌ Incorrect

- Managed Volumes can store:

  - Structured

  - Semi-structured

  - Unstructured files

**D. It requires an External Location.** ❌ Incorrect

- Only External Volumes require an External Location.

**E. It cannot be accessed with DBUtils.** ❌ Incorrect

- DBUtils works very well with Volumes.

------------------------------------------------------------------------

**Memory Trick**

Managed Volume

↓

Databricks manages storage.

------------------------------------------------------------------------

# [README](./../../../README.md)
