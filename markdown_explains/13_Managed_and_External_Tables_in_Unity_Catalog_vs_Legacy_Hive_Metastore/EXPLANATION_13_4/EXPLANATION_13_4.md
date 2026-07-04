# EXPLANATION 13 4

**Question 4**

**What is the primary difference between a managed table and an external table in Unity Catalog?**

**Correct Answer:**\
✅ **Managed tables store data in Unity Catalog-managed storage, while external tables store data in a user-defined ADLS location.**

**Explanation**

**Managed Table**

Unity Catalog manages:

- Storage location

- Metadata

- File placement

Unity Catalog\
\
↓\
\
Chooses Storage

**External Table**

The customer chooses the storage location.

Customer\
\
↓\
\
Chooses Storage

Example:

LOCATION 'abfss://finance@storage.dfs.core.windows.net/'

**Comparison**

| **Managed**                | **External**                     |
|----------------------------|----------------------------------|
| Databricks chooses storage | Customer chooses storage         |
| Simpler administration     | Greater flexibility              |
| Best for managed data      | Best for shared or existing data |

**YouTube**

**Managed vs External Tables**

https://www.youtube.com/results?search_query=Managed+vs+External+Tables+Databricks

# [README](./../../../README.md)
