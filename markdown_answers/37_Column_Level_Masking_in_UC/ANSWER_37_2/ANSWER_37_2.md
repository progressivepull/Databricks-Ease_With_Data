# ANSWER 37 2

**Question 2**

**How does Column-Level Masking differ from Row-Level Security?**

**A. Column-Level Masking hides entire rows, while Row-Level Security hides columns. ❌ Incorrect**

This reverses their purposes.

Correct relationship:

- RLS → rows

- Masking → columns

**B. Column-Level Masking protects individual column values, while Row-Level Security controls which rows are visible. ✅ Correct**

Think of them like this:

**Row-Level Security**

Table

↓

Remove unauthorized rows

**Column Masking**

Table

↓

Keep rows

↓

Mask selected columns

Example:

Without security:

| **Employee** | **Salary** |
|--------------|------------|
| John         | 100000     |
| Mary         | 90000      |

With Row-Level Security:

John only sees:

| **Employee** | **Salary** |
|--------------|------------|
| John         | 100000     |

With Column Masking:

| **Employee** | **Salary**   |
|--------------|--------------|
| John         | \*\*\*\*\*\* |
| Mary         | \*\*\*\*\*\* |

Rows remain visible.

Values change.

**C. Both features perform exactly the same function. ❌ Incorrect**

They solve different security problems.

**D. Row-Level Security works only with SQL, while Column-Level Masking works only with PySpark. ❌ Incorrect**

Both integrate with Unity Catalog regardless of whether users query with SQL or supported APIs.

**E. Column-Level Masking requires separate tables for each user. ❌ Incorrect**

One shared table is the entire advantage.

**Why B is correct**

Row-Level Security controls **which rows** are returned.

Column-Level Masking controls **what values** users see in specific columns.

# [README](./../../../README.md)
