# ANSWER 10 2

**Question 2**

**According to Databricks best practices, how many metastores should generally be created per cloud region?**

**A. One metastore per workspace** ❌ Incorrect

- This defeats the purpose of centralized governance.

- Multiple workspaces should share the same metastore whenever possible.

**B. One metastore per catalog** ❌ Incorrect

- A single metastore can contain many catalogs.

Example:

Metastore\
├── Finance\
├── Sales\
├── HR\
└── Engineering

**C. One metastore per cloud region** ✅ Correct

Databricks recommends:

- One metastore for each cloud region.

- All workspaces in that region attach to it.

Benefits:

- Centralized permissions

- Easier administration

- Shared catalogs

- Consistent governance

**D. One metastore per user** ❌ Incorrect

- Metastores are organization-wide resources, not personal resources.

**E. One metastore per storage account** ❌ Incorrect

- A metastore is independent of the number of storage accounts.

**Memory Trick**

Think:

One Region\
↓\
One Metastore

# [README](./../../../README.md)
