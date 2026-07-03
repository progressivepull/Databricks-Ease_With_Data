# ANSWER 08 3

**Question 3**

**Which object is the top-level container in the Unity Catalog hierarchy?**

**A. Catalog** ❌ Incorrect

- Catalog is high-level but **not the highest**.

**B. Schema** ❌ Incorrect

- Schemas live inside catalogs.

**C. Table** ❌ Incorrect

- Tables live inside schemas.

**D. Metastore** ✅ Correct

Hierarchy:

Metastore\
↓\
Catalog\
↓\
Schema\
↓\
Table/View/Volume/Function

The metastore manages:

- All metadata

- Catalogs

- Permissions

- Governance

Usually an organization has **one metastore per region**.

**E. Volume** ❌ Incorrect

- Volumes store files.

- They are much lower in the hierarchy.

**Memory trick**

Think of a filing cabinet:

Building = Metastore\
Room = Catalog\
Cabinet = Schema\
Folder = Table

------------------------------------------------------------------------

# [README](./../../../README.md)
