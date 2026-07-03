# ANSWER 08 2

**Question 2**

**What is the core principle of Unity Catalog?**

**A. Store data in multiple locations for redundancy.** ❌ Incorrect

- Data redundancy is handled by cloud storage systems.

- Unity Catalog manages permissions—not data replication.

**B. Define security once and enforce it everywhere.** ✅ Correct

This is the biggest benefit of Unity Catalog.

Without Unity Catalog:

- Workspace A has one set of permissions.

- Workspace B has another.

- Workspace C has another.

Administrators spend lots of time keeping them synchronized.

With Unity Catalog:

- Define permissions once.

- Every attached workspace automatically follows them.

This is called **centralized governance**.

**C. Use one workspace for every department.** ❌ Incorrect

- Organizations often have many workspaces.

- Unity Catalog is specifically designed to manage many workspaces.

**D. Create a separate metastore for every catalog.** ❌ Incorrect

- One metastore can contain many catalogs.

- The hierarchy is:

Metastore\
├── Catalog\
├── Catalog\
└── Catalog

**E. Replace cloud storage with Databricks-managed storage.** ❌ Incorrect

- Unity Catalog does not replace Azure Storage, S3, or GCS.

- Data remains in your cloud storage.

**Key idea**

**Define permissions once → Enforced everywhere**

------------------------------------------------------------------------

# [README](./../../../README.md)
