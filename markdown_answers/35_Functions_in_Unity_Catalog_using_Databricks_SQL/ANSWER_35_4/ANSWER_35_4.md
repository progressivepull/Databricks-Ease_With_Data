# ANSWER 35 4

**Question 4**

**What distinguishes a scalar function from a table function?**

**A. Scalar functions are written only in SQL, while table functions are written only in Python. ❌ Incorrect**

Both can be written in SQL.

------------------------------------------------------------------------

**B. Scalar functions return one value, while table functions return multiple rows. ✅ Correct**

Example:

Scalar:

tax(100)

Returns:

7

One value.

Table function:

SELECT \*

FROM employee_lookup()

Returns:

| **ID** | **Name** |
|--------|----------|
| 1      | John     |
| 2      | Mary     |

Multiple rows.

------------------------------------------------------------------------

**C. Scalar functions require parameters, while table functions do not. ❌ Incorrect**

Both may have parameters.

------------------------------------------------------------------------

**D. Scalar functions can only be used in PySpark. ❌ Incorrect**

They are commonly used in SQL.

------------------------------------------------------------------------

**E. Table functions cannot access tables. ❌ Incorrect**

Table functions often query tables.

------------------------------------------------------------------------

**Why B is correct**

The difference is determined by **what is returned**, not how the function is written.

# [README](./../../../README.md)
