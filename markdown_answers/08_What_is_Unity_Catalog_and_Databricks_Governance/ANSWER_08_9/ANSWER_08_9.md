# ANSWER 08 9

**Question 9**

**How are tables referenced in Unity Catalog?**

**A. table** ❌ Incorrect

- Ambiguous.

- Different schemas could contain the same table name.

**B. schema.table** ❌ Incorrect

- Missing the catalog.

**C. workspace.schema.table** ❌ Incorrect

- Workspace is not part of the naming convention.

**D. catalog.schema.table** ✅ Correct

Example:

sales.finance.transactions

Where:

- sales = Catalog

- finance = Schema

- transactions = Table

This uniquely identifies the table.

**E. metastore.catalog.table** ❌ Incorrect

- Metastore is not included in SQL object references.

**Memory trick**

catalog.schema.table

Always remember this three-part naming convention.

# [README](./../../../README.md)
