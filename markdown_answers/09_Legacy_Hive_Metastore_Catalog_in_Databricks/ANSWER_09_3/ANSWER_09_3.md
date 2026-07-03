# ANSWER 09 3

**Question 3**

**If no schema is specified when creating a table in the Hive Metastore, where is the table created?**

**A. Bronze schema** ❌ Incorrect

- Bronze is a Medallion Architecture naming convention.

- It is not automatically created by Hive Metastore.

**B. Information Schema** ❌ Incorrect

- INFORMATION_SCHEMA contains metadata about database objects.

- It is not used for storing user tables.

**C. Default schema** ✅ Correct

If you write:

CREATE TABLE employees (...)

Databricks assumes:

default.employees

unless another schema is selected with:

USE sales;

**D. Unity Catalog schema** ❌ Incorrect

- Hive Metastore predates Unity Catalog.

**E. System schema** ❌ Incorrect

- System schemas are reserved for system metadata.

**Key Concept**

If you don't specify a schema:

default.table_name

------------------------------------------------------------------------

# [README](./../../../README.md)
