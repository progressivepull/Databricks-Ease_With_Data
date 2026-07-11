# ANSWER 43 3

**Question 3**

**What Unity Catalog object represents external data accessed through a live connection?**

**A. Managed Catalog** ❌ Incorrect

- Managed catalogs contain Databricks-managed objects.

**B. Delta Catalog** ❌ Incorrect

- There is no Unity Catalog object called a Delta Catalog.

**C. Foreign Catalog** ✅ Correct

- A Foreign Catalog represents an external database.

- Inside it are foreign schemas and foreign tables.

Example:

Unity Catalog

│

Foreign Catalog

│

Foreign Schema

│

Foreign Tables

**D. Shared Volume** ❌ Incorrect

- Volumes store files.

- They are unrelated to Federation.

**E. External Pipeline** ❌ Incorrect

- No such Unity Catalog object exists.

**Key Concept**

**External Database = Foreign Catalog**

# [README](./../../../README.md)
