# ANSWER 37 4

**Question 4**

**In the metadata-driven masking approach, what is the primary purpose of the metadata table?**

**A. To store Spark cluster information ❌ Incorrect**

Cluster settings belong to Databricks Compute.

**B. To maintain mappings between users and their authorization groups or roles ✅ Correct**

Example:

| **User** | **Group** |
|----------|-----------|
| John     | HR        |
| Mary     | Finance   |
| Bob      | Managers  |

The masking function checks:

Current User

↓

Metadata Table

↓

Authorized?

↓

Original Value

or

Masked Value

Changing permissions requires updating only the metadata table.

**C. To cache masked values for faster queries ❌ Incorrect**

Masking is evaluated dynamically.

**D. To replace Unity Catalog permissions ❌ Incorrect**

Metadata complements Unity Catalog.

It doesn't replace object permissions.

**E. To store Delta transaction logs ❌ Incorrect**

Those live in:

\_delta_log

**Why B is correct**

The metadata table centralizes authorization rules, making masking easier to maintain.

# [README](./../../../README.md)
