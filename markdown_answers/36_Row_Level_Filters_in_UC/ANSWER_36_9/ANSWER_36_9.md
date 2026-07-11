# ANSWER 36 9

**Question 9**

**How can an administrator grant a user access to an additional market segment without modifying the row filter function?**

**A. Rewrite the SQL function. ❌ Incorrect**

That would require unnecessary code changes.

------------------------------------------------------------------------

**B. Recreate the table. ❌ Incorrect**

The table structure hasn't changed.

------------------------------------------------------------------------

**C. Update the metadata table with the new authorization rule. ✅ Correct**

Example:

Before:

| **User** | **Region** |
|----------|------------|
| John     | East       |

Administrator adds:

| **User** | **Region** |
|----------|------------|
| John     | West       |

The function stays exactly the same.

Only the metadata changes.

This is one of the biggest advantages of metadata-driven security.

------------------------------------------------------------------------

**D. Restart the Databricks cluster. ❌ Incorrect**

Security changes don't require cluster restarts.

------------------------------------------------------------------------

**E. Create a separate table for the user. ❌ Incorrect**

That defeats the purpose of Row-Level Security.

------------------------------------------------------------------------

**Why C is correct**

The security rules live in the metadata table, allowing administrators to change access without modifying application logic.

------------------------------------------------------------------------

# [README](./../../../README.md)
