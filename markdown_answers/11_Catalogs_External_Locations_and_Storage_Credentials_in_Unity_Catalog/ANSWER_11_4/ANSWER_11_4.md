# ANSWER 11 4

**Question 4**

**Which schemas are automatically created when a new catalog is created?**

**A. bronze and silver** ❌ Incorrect

- Bronze and Silver are Medallion Architecture conventions.

- Databricks does not automatically create them.

**B. public and system** ❌ Incorrect

- These are not automatically created user schemas.

**C. default and information_schema** ✅ Correct

Every new catalog includes:

**default**

- Used for creating objects without specifying another schema.

**information_schema**

Contains metadata such as:

- Tables

- Columns

- Views

- Privileges

- Catalog information

**D. dev and prod** ❌ Incorrect

- Organizations may create these manually.

**E. catalog and schema** ❌ Incorrect

- These are object types, not schema names.

**Memory Trick**

Every catalog starts with:

default\
information_schema

# [README](./../../../README.md)
