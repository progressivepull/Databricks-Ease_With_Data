# ANSWER 36 4

**Question 4**

**What is the purpose of the metadata table used in the lesson?**

**A. To store Spark cluster configurations ❌ Incorrect**

- Cluster settings belong to Databricks Compute.

------------------------------------------------------------------------

**B. To store Delta transaction logs ❌ Incorrect**

- Delta transaction logs are stored in:

\_delta_log

------------------------------------------------------------------------

**C. To centrally maintain user authorization rules, such as which market segments each user may access. ✅ Correct**

Example metadata table:

| **User** | **Region** |
|----------|------------|
| John     | East       |
| Mary     | West       |
| Bob      | North      |

The row filter checks:

Current User

↓

Metadata Table

↓

Authorized?

↓

TRUE/FALSE

Changing security means updating the metadata—not the function.

------------------------------------------------------------------------

**D. To cache query results for faster execution ❌ Incorrect**

- Caching is unrelated.

------------------------------------------------------------------------

**E. To store notebook permissions only ❌ Incorrect**

- Notebook permissions are managed separately.

------------------------------------------------------------------------

**Why C is correct**

The metadata table centralizes authorization rules, making security easier to maintain.

------------------------------------------------------------------------

# [README](./../../../README.md)
