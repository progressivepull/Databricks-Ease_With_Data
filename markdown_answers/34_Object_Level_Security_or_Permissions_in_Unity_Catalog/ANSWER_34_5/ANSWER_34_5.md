# ANSWER 34 5

**Question 5**

**Which combination of privileges is required for a user to successfully query a Unity Catalog table?**

**A. SELECT only ❌ Incorrect**

SELECT allows reading data.

But first the user must be able to navigate:

Catalog\
→ Schema\
→ Table

**B. USE CATALOG and SELECT only ❌ Incorrect**

Missing:

USE SCHEMA

Without it, the table cannot be reached.

**C. USE SCHEMA and SELECT only ❌ Incorrect**

Missing:

USE CATALOG

**D. USE CATALOG, USE SCHEMA, and SELECT ✅ Correct**

To read a table you need:

1.  USE CATALOG

2.  USE SCHEMA

3.  SELECT

Think of entering a building:

Building

↓

Floor

↓

Room

Equivalent:

Catalog

↓

Schema

↓

Table

Need permission at every step.

**E. BROWSE and SELECT only ❌ Incorrect**

BROWSE lets you discover objects.

It does not replace:

- USE CATALOG

- USE SCHEMA

**Why D is correct**

All three privileges are required to successfully query a Unity Catalog table.

# [README](./../../../README.md)
