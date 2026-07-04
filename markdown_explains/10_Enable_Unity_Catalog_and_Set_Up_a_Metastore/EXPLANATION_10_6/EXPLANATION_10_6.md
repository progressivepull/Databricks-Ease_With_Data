# EXPLANATION 10 6

**Question 6**

**Which Azure RBAC role must be assigned to the Access Connector so it can access the storage account?**

**Correct Answer:**\
✅ **Storage Blob Data Contributor**

**Explanation**

The Access Connector requires permission to:

- Read files

- Write files

- Delete files

- Create folders

The recommended Azure RBAC role is:

**Storage Blob Data Contributor**

This role provides the data access needed without granting broader administrative permissions.

Example:

Managed Identity\
\
↓\
\
Storage Blob Data Contributor\
\
↓\
\
Azure Storage

This follows Azure's principle of least privilege.

**YouTube**

**Azure RBAC for Databricks**

https://www.youtube.com/results?search_query=Azure+RBAC+Databricks

# [README](./../../../README.md)
