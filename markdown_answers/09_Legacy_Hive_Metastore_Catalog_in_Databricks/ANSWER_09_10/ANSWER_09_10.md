# ANSWER 09 10

**Question 10**

**Which statement best describes a view in the Hive Metastore?**

**A. A view stores a physical copy of the underlying table data.** ❌ Incorrect

- A standard view does **not** duplicate data.

- (Materialized views are a separate concept.)

**B. A view stores only a SQL query and does not duplicate the underlying data.** ✅ Correct

Example:

CREATE VIEW high_salary AS\
SELECT \*\
FROM employees\
WHERE salary \> 100000;

The view stores only:

SELECT \*\
FROM employees\
WHERE salary \> 100000;

Whenever you query the view, Databricks executes that SQL against the current data.

**C. A view can only be queried once.** ❌ Incorrect

- Views can be queried indefinitely.

**D. A view automatically creates a Delta table.** ❌ Incorrect

- A view references existing tables; it does not create new ones.

**E. A view cannot persist after restarting the compute cluster.** ❌ Incorrect

- Views are metadata objects stored in the metastore and remain available after clusters restart.

**Memory Trick**

A view is like a **saved SQL query**:

View\
↓\
Stores SQL\
\
Table\
↓\
Stores Data

------------------------------------------------------------------------

**Summary Table**

| **Concept** | **Hive Metastore** |
|----|----|
| Default catalog before Unity Catalog | Hive Metastore |
| Namespace format | schema.table |
| Default schema | default |
| Managed table | Databricks manages metadata and data files |
| Managed table storage | DBFS (traditionally) |
| External table | User specifies the storage location |
| Drop managed table | Deletes both metadata and data files |
| Drop external table | Deletes only metadata; data files remain |
| Recreate external table | Possible because the underlying data still exists |
| View | Stores a SQL query, not a copy of the data |

# [README](./../../../README.md)
