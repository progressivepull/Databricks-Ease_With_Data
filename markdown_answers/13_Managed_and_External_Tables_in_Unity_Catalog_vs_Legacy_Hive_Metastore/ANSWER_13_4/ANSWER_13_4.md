# ANSWER 13 4

**Question 4**

**What is the primary difference between a managed table and an external table in Unity Catalog?**

**A. Managed tables cannot store Delta data.** ❌ Incorrect

- Managed tables commonly use Delta Lake.

Example:

CREATE TABLE sales USING DELTA;

**B. External tables store metadata only.** ❌ Incorrect

- External tables have both:

  - Metadata in Unity Catalog

  - Data in external storage

**C. Managed tables store data in Unity Catalog-managed storage, while external tables store data in a user-defined ADLS location.** ✅ Correct

Managed Table:

Unity Catalog\
↓\
Chooses storage

External Table:

User\
↓\
Chooses storage

This is the biggest distinction.

**D. Managed tables require SQL, while external tables require Python.** ❌ Incorrect

- Both can be created using SQL.

**E. External tables cannot be queried.** ❌ Incorrect

- External tables are queried exactly like managed tables.

**Memory Trick**

Managed = Databricks manages storage

External = You manage storage

------------------------------------------------------------------------

# [README](./../../../README.md)
