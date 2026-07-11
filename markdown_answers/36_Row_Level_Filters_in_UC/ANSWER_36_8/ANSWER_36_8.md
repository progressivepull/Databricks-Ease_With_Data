# ANSWER 36 8

**Question 8**

**What happens after a row filter is attached directly to a Unity Catalog table?**

**A. Users must manually include a WHERE clause in every query. ❌ Incorrect**

That's exactly what row filters eliminate.

------------------------------------------------------------------------

**B. Only administrators can query the table. ❌ Incorrect**

Anyone with permission can query the table.

They simply see different rows.

------------------------------------------------------------------------

**C. Unity Catalog automatically applies the filter to every query against the table. ✅ Correct**

Suppose a user runs:

SELECT \*

FROM sales

Unity Catalog automatically behaves as though it executed:

SELECT \*

FROM sales

WHERE security_function(...)

The filtering is transparent.

------------------------------------------------------------------------

**D. The table becomes read-only. ❌ Incorrect**

Read/write permissions are separate.

------------------------------------------------------------------------

**E. The table is converted into a dynamic view. ❌ Incorrect**

The object remains a table.

------------------------------------------------------------------------

**Why C is correct**

Once attached, the row filter is automatically enforced for every query against the table.

------------------------------------------------------------------------

# [README](./../../../README.md)
