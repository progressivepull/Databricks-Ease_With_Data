# ANSWER 39 7

**Question 7**

**Which permissions are typically required before a provider can include objects in a Delta Share?**

**A. MODIFY, DELETE, and DROP ❌ Incorrect**

These permissions modify data.

Sharing requires read-related permissions.

**B. CREATE TABLE, CREATE VIEW, and CREATE FUNCTION ❌ Incorrect**

Creation privileges are unrelated.

**C. SELECT for tables, READ VOLUME for volumes, and EXECUTE for functions ✅ Correct**

Each object requires its corresponding privilege:

| **Object** | **Required Privilege** |
|------------|------------------------|
| Table      | SELECT                 |
| Volume     | READ VOLUME            |
| Function   | EXECUTE                |

The provider must already have these permissions before sharing the object.

**D. MANAGE and OWNERSHIP only ❌ Incorrect**

Management privileges alone are insufficient without access to the objects being shared.

**E. CREATE SHARE only ❌ Incorrect**

Creating a Share is only one step.

The provider must also be authorized to include the objects.

**Why C is correct**

The provider must have the appropriate permissions for each object type before adding it to a Delta Share.

# [README](./../../../README.md)
