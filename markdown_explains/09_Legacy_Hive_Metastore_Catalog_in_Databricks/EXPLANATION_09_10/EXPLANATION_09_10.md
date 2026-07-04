# EXPLANATION 09 10

**Question 10**

**Which statement best describes a view in the Hive Metastore?**

**Correct Answer:**\
✅ **A view stores only a SQL query and does not duplicate the underlying data.**

**Explanation**

A **view** does not contain data.

Instead, it stores a SQL statement.

Example:

CREATE VIEW high_salary AS\
\
SELECT \*\
\
FROM employees\
\
WHERE salary \> 100000;

The view stores only the SQL definition.

Whenever someone queries the view:

SELECT \*\
\
FROM high_salary;

Databricks runs the stored SQL against the underlying table.

**Comparison**

| **Table**        | **View**                     |
|------------------|------------------------------|
| Stores data      | Stores SQL                   |
| Occupies storage | Very little storage          |
| Independent      | Depends on underlying tables |

Views simplify complex queries without duplicating data.

**YouTube**

**Databricks Views Explained**

https://www.youtube.com/results?search_query=Databricks+Views+Tutorial

**Recommended YouTube Playlists**

If you're studying Hive Metastore and Unity Catalog together, these playlists are excellent resources:

1.  **Official Databricks – Unity Catalog**

    - https://www.youtube.com/results?search_query=Databricks+Unity+Catalog

2.  **Hive Metastore vs Unity Catalog**

    - https://www.youtube.com/results?search_query=Hive+Metastore+vs+Unity+Catalog

3.  **Managed vs External Tables**

    - https://www.youtube.com/results?search_query=Managed+vs+External+Tables+Databricks

4.  **Databricks Administration**

    - https://www.youtube.com/results?search_query=Databricks+Administration

5.  **Azure Databricks Full Course**

    - https://www.youtube.com/results?search_query=Azure+Databricks+Full+Course

# [README](./../../../README.md)
