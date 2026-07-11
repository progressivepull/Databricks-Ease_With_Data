# ANSWER 35 10

**Question 10**

**Which statement correctly describes function parameters and function types?**

**A. Functions with multiple parameters are always table functions. ❌ Incorrect**

Example:

tax(price, rate)

This has two parameters but still returns one value.

It is a scalar function.

------------------------------------------------------------------------

**B. Functions with no parameters must be scalar functions. ❌ Incorrect**

A table function may also have no parameters.

Example:

SELECT \*

FROM active_customers();

Returns many rows.

------------------------------------------------------------------------

**C. The number of parameters determines whether a function is scalar or table. ❌ Incorrect**

Parameters do **not** determine the function type.

You can have:

- one parameter

- ten parameters

- no parameters

and still have either a scalar or table function.

------------------------------------------------------------------------

**D. The output determines the function type: one value is a scalar function, while multiple rows form a table function. ✅ Correct**

The defining characteristic is the **return value**:

**Scalar Function**

Input

↓

One Value

Example:

tax(100)

Returns:

7

**Table Function**

Input

↓

Multiple Rows

Example:

SELECT \*

FROM employee_lookup();

Returns:

| **ID** | **Name** |
|--------|----------|
| 1      | John     |
| 2      | Mary     |

------------------------------------------------------------------------

**E. Table functions cannot accept parameters. ❌ Incorrect**

Table functions can absolutely accept parameters.

Example:

SELECT \*

FROM employee_lookup(100);

Here, 100 is a parameter that influences the rows returned.

------------------------------------------------------------------------

**Why D is correct**

The distinction between **scalar** and **table** functions is based entirely on **what they return**:

- **Scalar function:** Returns a single value (such as a number, string, or date) for each invocation.

- **Table function:** Returns a result set consisting of multiple rows and columns that can be queried in the FROM clause.

The **number of parameters** has no bearing on the function type; only the **shape of the output** determines whether a function is scalar or table-valued.

# [README](./../../../README.md)
