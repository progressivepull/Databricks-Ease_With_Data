# ANSWER 34 3

**Question 3**

**What happens when a privilege is granted on a parent object, such as a Catalog?**

**A. Permissions apply only to the Catalog itself. ❌ Incorrect**

- Unity Catalog supports inheritance.

- Permissions can flow downward.

**B. Child objects automatically inherit the permission. ✅ Correct**

Example:

Catalog

↓

Schema

↓

Tables

If you grant:

GRANT USE CATALOG

on the Catalog, child objects inherit the appropriate permissions according to Unity Catalog's inheritance model.

This greatly simplifies administration.

**C. All existing permissions on child objects are removed. ❌ Incorrect**

Granting permissions does not remove existing permissions.

**D. Only Metastore Administrators receive the permission. ❌ Incorrect**

Permissions apply to the specified user or group.

**E. The permission applies only after a manual refresh. ❌ Incorrect**

Permission changes take effect without requiring a manual refresh.

**Why B is correct**

Unity Catalog uses **permission inheritance**, allowing parent-level grants to simplify access management.

# [README](./../../../README.md)
