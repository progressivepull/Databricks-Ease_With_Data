# ANSWER 35 5

**Question 5**

**What is the benefit of using CREATE OR REPLACE FUNCTION?**

**A. It automatically grants permissions to all users. ❌ Incorrect**

Permissions remain unchanged.

------------------------------------------------------------------------

**B. It allows a function to be updated without manually dropping it first. ✅ Correct**

Instead of:

DROP FUNCTION tax;

CREATE FUNCTION tax...

You simply write:

CREATE OR REPLACE FUNCTION tax...

This is:

- safer

- simpler

- cleaner

------------------------------------------------------------------------

**C. It converts a scalar function into a table function. ❌ Incorrect**

Function type depends on its definition.

------------------------------------------------------------------------

**D. It automatically creates a new catalog and schema. ❌ Incorrect**

Catalogs must already exist.

------------------------------------------------------------------------

**E. It changes a SQL function into a Python function. ❌ Incorrect**

Language is specified separately.

**Why B is correct**

CREATE OR REPLACE FUNCTION lets you modify an existing function without explicitly dropping it first.

------------------------------------------------------------------------

# [README](./../../../README.md)
