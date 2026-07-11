# ANSWER 34 6

**Question 6**

**What does the BROWSE privilege allow a user to do?**

**A. Read data from tables and views ❌ Incorrect**

That requires:

SELECT

**B. Modify table data ❌ Incorrect**

That requires:

MODIFY

**C. Discover catalogs, view metadata, and see lineage without accessing the data itself ✅ Correct**

BROWSE allows users to:

- discover catalogs

- see schemas

- inspect metadata

- view lineage

- search for data assets

But **not** read table contents.

Example:

Sales Catalog

↓

Orders Table

User can see:

- table exists

- columns

- owner

- lineage

But cannot run:

SELECT \*

**D. Create new schemas and tables ❌ Incorrect**

Requires:

CREATE

**E. Drop Unity Catalog objects ❌ Incorrect**

Requires:

MANAGE

or ownership.

**Why C is correct**

BROWSE improves discoverability while keeping data secure.

# [README](./../../../README.md)
