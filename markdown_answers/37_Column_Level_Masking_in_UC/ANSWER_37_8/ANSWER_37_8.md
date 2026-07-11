# ANSWER 37 8

**Question 8**

**What is the purpose of the built-in is_member() function?**

**A. To determine whether a table contains duplicate rows ❌ Incorrect**

Duplicate detection is unrelated.

**B. To check whether the current user belongs to a specified group ✅ Correct**

Example:

is_member('Managers')

Returns:

TRUE

if the current user belongs to Managers.

Otherwise:

FALSE

This eliminates the need for custom lookup tables in many scenarios.

**C. To verify whether a Spark cluster is active ❌ Incorrect**

Clusters are unrelated.

**D. To retrieve the current user's email address ❌ Incorrect**

That's:

CURRENT_USER()

**E. To determine whether a table exists in Unity Catalog ❌ Incorrect**

No connection to table existence.

**Why B is correct**

is_member() checks group membership, making authorization logic much simpler.

# [README](./../../../README.md)
