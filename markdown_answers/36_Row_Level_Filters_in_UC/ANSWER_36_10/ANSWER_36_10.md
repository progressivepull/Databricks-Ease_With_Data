# ANSWER 36 10

**Question 10**

**Which statement correctly compares Dynamic Views and Row-Level Filters?**

**A. Both automatically apply security to every table query without additional configuration. ❌ Incorrect**

Dynamic Views only apply when users query the **view**, not the underlying table.

------------------------------------------------------------------------

**B. Dynamic Views require users to query the view, while Row-Level Filters automatically enforce security on all queries against the table. ✅ Correct**

Comparison:

| **Dynamic View** | **Row-Level Filter** |
|----|----|
| User queries the view | User queries the table |
| Security logic is inside the view | Security is attached to the table |
| Users must use the view | Automatic enforcement on every table query |

Example:

Dynamic View:

SELECT \*

FROM secure_sales_view

Row-Level Filter:

SELECT \*

FROM sales

The filter is automatically applied by Unity Catalog.

------------------------------------------------------------------------

**C. Row-Level Filters cannot use Boolean functions. ❌ Incorrect**

They **must** use Boolean logic because the function returns TRUE or FALSE for each row.

------------------------------------------------------------------------

**D. Dynamic Views can only filter columns, not rows. ❌ Incorrect**

Dynamic Views can filter both:

- rows

- columns

- even mask sensitive data

------------------------------------------------------------------------

**E. Row-Level Filters require users to manually call a security function in every query. ❌ Incorrect**

The major benefit of Row-Level Filters is that users **do not** need to call the security function themselves.

Unity Catalog enforces it automatically.

------------------------------------------------------------------------

**Why B is correct**

Dynamic Views and Row-Level Filters both implement row-level security, but they differ in **how the security is enforced**:

- **Dynamic Views** require users to query the secure view. If someone queries the underlying table directly (and has permission), the view's logic is bypassed.

- **Row-Level Filters** are attached directly to the table. Every query against that table automatically evaluates the row filter function, ensuring consistent enforcement regardless of who queries the table or how they write the SQL.

For enterprise environments, Row-Level Filters provide stronger, centralized enforcement because the security travels with the table itself rather than depending on users to access a specific view.

# [README](./../../../README.md)
