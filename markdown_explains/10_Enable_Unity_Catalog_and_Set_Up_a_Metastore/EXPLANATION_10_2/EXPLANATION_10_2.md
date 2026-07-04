# EXPLANATION 10 2

**Question 2**

**According to Databricks best practices, how many metastores should generally be created per cloud region?**

**Correct Answer:**\
✅ **One metastore per cloud region**

**Explanation**

Databricks recommends **one Metastore per cloud region**.

Example:

East US\
│\
▼\
One Metastore\
\
│\
┌────┼─────┐\
▼ ▼ ▼\
Workspace A\
Workspace B\
Workspace C

Benefits include:

- Centralized governance

- Easier administration

- Shared catalogs

- Consistent permissions

- Simplified auditing

Creating multiple metastores in the same region is generally discouraged unless there is a specific business or regulatory requirement.

**Memory Trick**

One Region\
\
↓\
\
One Metastore

**YouTube**

**Unity Catalog Best Practices**

https://www.youtube.com/results?search_query=Unity+Catalog+Best+Practices

# [README](./../../../README.md)
