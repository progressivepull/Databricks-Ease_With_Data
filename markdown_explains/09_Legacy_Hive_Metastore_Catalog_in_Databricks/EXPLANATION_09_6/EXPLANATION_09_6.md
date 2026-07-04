# EXPLANATION 09 6

**Question 6**

**What is the primary difference between a managed table and an external table?**

**Correct Answer:**\
✅ **External tables require a user-defined storage location, while managed tables do not.**

**Explanation**

**Managed Table**

Databricks determines where data is stored.

CREATE TABLE\
\
↓\
\
Databricks Chooses Storage

**External Table**

The user chooses the storage location.

Example:

LOCATION\
'abfss://sales@storage.dfs.core.windows.net/data'

The customer owns the storage.

**Comparison**

| **Managed Table**          | **External Table**      |
|----------------------------|-------------------------|
| Databricks manages storage | User manages storage    |
| Easier administration      | Greater flexibility     |
| Data deleted when dropped  | Data remains after drop |

**YouTube**

**Managed vs External Tables**

https://www.youtube.com/results?search_query=Managed+vs+External+Tables+Databricks

# [README](./../../../README.md)
