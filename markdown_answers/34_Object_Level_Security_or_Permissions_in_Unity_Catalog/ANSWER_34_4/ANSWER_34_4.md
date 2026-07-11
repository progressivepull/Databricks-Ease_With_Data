# ANSWER 34 4

**Question 4**

**When is the top-down permission model most appropriate?**

**A. When granting access to only one specific table ❌ Incorrect**

- Table-level permissions are better for very specific access.

**B. When users need broad access to an entire Catalog or Schema through inherited permissions ✅ Correct**

Suppose a Finance team needs access to everything:

Finance Catalog

↓

All Schemas

↓

All Tables

Instead of granting hundreds of permissions individually:

Grant once:

Finance Catalog

Everything underneath inherits access.

**C. When hiding catalogs from all users ❌ Incorrect**

Top-down permissions are about granting access efficiently, not hiding objects.

**D. When granting MANAGE privileges only ❌ Incorrect**

Top-down permissions apply to many privilege types.

**E. When assigning permissions to Spark clusters ❌ Incorrect**

Clusters are unrelated.

**Why B is correct**

Top-down permissions reduce administrative work by allowing inherited access across many objects.

# [README](./../../../README.md)
