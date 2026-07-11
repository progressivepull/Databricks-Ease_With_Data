# ANSWER 35 3

**Question 3**

**What is the primary advantage of a Unity Catalog User-Defined Function (UDF) over a PySpark session UDF?**

**A. It executes only in Python. ❌ Incorrect**

Unity Catalog functions can be written in SQL or Python.

------------------------------------------------------------------------

**B. It is available only within the current notebook session. ❌ Incorrect**

That's the opposite.

Session UDFs are temporary.

Unity Catalog UDFs are permanent.

------------------------------------------------------------------------

**C. It is permanently registered, shared across users, and governed by Unity Catalog permissions. ✅ Correct**

Comparison:

| **Session UDF**      | **Unity Catalog UDF**                          |
|----------------------|------------------------------------------------|
| Temporary            | Permanent                                      |
| Current session only | Available across workspaces (with permissions) |
| No governance        | Unity Catalog governance                       |
| Must recreate        | Registered once                                |

------------------------------------------------------------------------

**D. It requires no registration. ❌ Incorrect**

Unity Catalog functions must be created using SQL.

Example:

CREATE FUNCTION ...

------------------------------------------------------------------------

**E. It can return only Boolean values. ❌ Incorrect**

Functions can return many data types.

------------------------------------------------------------------------

**Why C is correct**

Unity Catalog UDFs are permanent, reusable, and centrally governed.

------------------------------------------------------------------------

# [README](./../../../README.md)
