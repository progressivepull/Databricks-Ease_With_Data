# ANSWER 05 4

**Question 4**

**What is the top-level container required before enabling Unity Catalog?**

**A. Catalog** ❌ Incorrect

- Catalogs are created **inside** a metastore.

- They are not the highest level.

**B. Schema** ❌ Incorrect

- Schemas exist inside catalogs.

Hierarchy:

Metastore\
└── Catalog\
└── Schema\
└── Tables

**C. Volume** ❌ Incorrect

- Volumes store non-tabular files.

- They are not the top-level object.

**D. Metastore** ✅ **Correct**

- Every Unity Catalog deployment starts with a metastore.

- The metastore stores:

  - Metadata

  - Permissions

  - Governance policies

  - Object definitions

**E. Workspace** ❌ Incorrect

- Workspaces attach to a metastore.

- A workspace alone cannot provide Unity Catalog governance.

**Key Concept**

Think of the metastore as the **master database of metadata** for Unity Catalog.

------------------------------------------------------------------------

# [README](./../../../README.md)
