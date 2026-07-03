# ANSWER 09 2

**Question 2**

**Which namespace format is used by the Hive Metastore?**

**A. catalog.schema.table** ❌ Incorrect

- This is the naming convention for **Unity Catalog**, not Hive Metastore.

Example:

sales.finance.orders

**B. workspace.catalog.table** ❌ Incorrect

- Workspaces are not part of SQL object names.

**C. schema.table** ✅ Correct

Hive Metastore only has:

Schema\
└── Table

Example:

sales.orders

There is **no catalog level**.

**D. catalog.table** ❌ Incorrect

- Missing the schema.

**E. table.schema** ❌ Incorrect

- SQL naming order is never reversed.

**Memory Trick**

**Hive Metastore**

schema.table

**Unity Catalog**

catalog.schema.table

------------------------------------------------------------------------

# [README](./../../../README.md)
