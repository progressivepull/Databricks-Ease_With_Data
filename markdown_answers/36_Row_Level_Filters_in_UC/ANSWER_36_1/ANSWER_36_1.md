# ANSWER 36 1

**Question 1**

**What is the primary purpose of Row-Level Security (RLS) in Unity Catalog?**

**A. To prevent users from accessing an entire Databricks workspace ❌ Incorrect**

- Workspace access is controlled through:

  - Workspace permissions

  - Identity providers (Azure AD, Okta, etc.)

  - Workspace administrators

- Row-Level Security works **inside a table**, not at the workspace level.

------------------------------------------------------------------------

**B. To encrypt sensitive columns in a table ❌ Incorrect**

- Encryption protects data at rest or in transit.

- RLS controls **which rows** a user is allowed to see.

- Column encryption and Row-Level Security solve different problems.

------------------------------------------------------------------------

**C. To restrict which rows each user can view within the same table ✅ Correct**

This is exactly what Row-Level Security (RLS) does.

Suppose the table contains:

| **Customer** | **Region** |
|--------------|------------|
| John         | East       |
| Mary         | West       |
| Bob          | East       |
| Alice        | North      |

East Manager sees:

| **Customer** | **Region** |
|--------------|------------|
| John         | East       |
| Bob          | East       |

West Manager sees:

| **Customer** | **Region** |
|--------------|------------|
| Mary         | West       |

Both query the **same physical table**, but Unity Catalog automatically filters the rows based on security rules.

------------------------------------------------------------------------

**D. To automatically create separate tables for each user ❌ Incorrect**

- That would create unnecessary duplication.

- RLS allows everyone to share **one table** while seeing different rows.

------------------------------------------------------------------------

**E. To hide SQL query text from users ❌ Incorrect**

- SQL visibility is unrelated to Row-Level Security.

------------------------------------------------------------------------

**Why C is correct**

Row-Level Security filters **rows**, not tables, columns, or workspaces.

------------------------------------------------------------------------

# [README](./../../../README.md)
