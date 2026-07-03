# ANSWER 14 6

**Question 6**

**How does a permanent view differ from a temporary view?**

**A. It stores all table data physically.** ❌ Incorrect

- Views never store table data.

**B. It persists after the compute cluster is restarted.** ✅ Correct

Permanent views are stored in Unity Catalog.

Example:

CREATE VIEW sales.high_salary AS\
SELECT \*\
FROM employees\
WHERE salary \> 100000;

Even after:

- Restart cluster

- Create new cluster

- Open tomorrow

The view still exists.

**C. It cannot reference Delta tables.** ❌ Incorrect

- Permanent views frequently reference Delta tables.

**D. It only supports Python queries.** ❌ Incorrect

- Views are queried using SQL.

**E. It requires Unity Catalog to be disabled.** ❌ Incorrect

- Unity Catalog fully supports permanent views.

**Memory Trick**

Temporary View

↓

Session

Permanent View

↓

Metastore

# [README](./../../../README.md)
