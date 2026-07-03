# ANSWER 13 3

**Question 3**

**Where is the data for a managed table stored when no storage location is specified?**

**A. In a user-defined ADLS directory** ❌ Incorrect

- This describes an external table.

**B. In Azure Key Vault** ❌ Incorrect

- Key Vault stores secrets, not table data.

**C. In Unity Catalog's managed storage location (catalog or metastore managed location)** ✅ Correct

Unity Catalog automatically chooses storage.

Priority:

Schema Managed Location\
↓\
Catalog Managed Location\
↓\
Metastore Managed Location

You do **not** specify a LOCATION clause.

**D. In GitHub repositories** ❌ Incorrect

- GitHub stores source code, not data files.

**E. Inside the notebook workspace** ❌ Incorrect

- Workspaces store notebooks, not managed table data.

**Key Concept**

Managed Table

↓

Unity Catalog chooses storage automatically.

------------------------------------------------------------------------

# [README](./../../../README.md)
