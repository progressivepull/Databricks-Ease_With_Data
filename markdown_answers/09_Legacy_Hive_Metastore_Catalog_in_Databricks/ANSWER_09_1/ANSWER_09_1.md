# ANSWER 09 1

**Question 1**

**Before Unity Catalog was introduced, what was the default catalog used by Databricks?**

**A. Unity Catalog** ❌ Incorrect

- Unity Catalog is the **modern governance system**, but it did not exist in the early versions of Databricks.

- Before Unity Catalog, Databricks relied on the **Hive Metastore** for storing table metadata.

**B. Delta Catalog** ❌ Incorrect

- There is **no Databricks component called Delta Catalog**.

- Delta Lake is a storage format, not a catalog.

**C. Hive Metastore** ✅ Correct

Before Unity Catalog:

- Databricks used the **Hive Metastore**.

- It stored:

  - Databases (schemas)

  - Tables

  - Views

  - Metadata

However, it lacked:

- Centralized governance

- Cross-workspace security

- Fine-grained permissions

- Data lineage

**D. Azure Catalog** ❌ Incorrect

- Azure has services like Azure Data Catalog and Microsoft Purview, but there is no Databricks component called **Azure Catalog**.

**E. Workspace Catalog** ❌ Incorrect

- There is no product named Workspace Catalog.

- Each workspace simply used its own Hive Metastore.

**Key Concept**

Think of the evolution:

Old Databricks\
│\
▼\
Hive Metastore\
\
Modern Databricks\
│\
▼\
Unity Catalog

------------------------------------------------------------------------

# [README](./../../../README.md)
