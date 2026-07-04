# EXPLANATION 14 6

**Question 6**

**How does a permanent view differ from a temporary view?**

**Correct Answer:**\
✅ **It persists after the compute cluster is restarted.**

**Explanation**

Permanent Views are stored in the metastore.

Example:

CREATE VIEW sales.high_salary AS\
SELECT \*\
FROM employees;

Even after:

- Restart Cluster

- Tomorrow

- Next Week

the view still exists.

**Comparison**

| **Temporary View**             | **Permanent View**                     |
|--------------------------------|----------------------------------------|
| Current session only           | Stored in Unity Catalog/Hive Metastore |
| Disappears after cluster stops | Remains until dropped                  |

**YouTube**

**Databricks Views**

https://www.youtube.com/results?search_query=Databricks+Views

# [README](./../../../README.md)
