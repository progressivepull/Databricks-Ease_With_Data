# ANSWER 37 10

**Question 10**

**Which combination of Unity Catalog security features provides a layered approach to data protection?**

**A. Delta Lake, Auto Loader, and DLT ❌ Incorrect**

These are data engineering technologies.

Not security layers.

**B. Object-Level Security, Row-Level Security, and Column-Level Masking ✅ Correct**

These three features work together to secure data at multiple levels:

**Layer 1 — Object-Level Security**

Controls access to objects.

Example:

Can you open this table?

**Layer 2 — Row-Level Security**

Controls rows.

Example:

Can you see East region rows?

**Layer 3 — Column-Level Masking**

Controls values.

Example:

Can you see the real salary?

Visualized together:

User

│

▼

Object-Level Security

(Can access table?)

│

▼

Row-Level Security

(Which rows?)

│

▼

Column Masking

(Which values?)

This layered approach provides comprehensive protection.

**C. Unity Catalog, MLflow, and Databricks SQL ❌ Incorrect**

MLflow manages machine learning.

Databricks SQL provides analytics.

They are not security layers.

**D. Catalogs, Schemas, and Volumes ❌ Incorrect**

These are Unity Catalog objects, not security mechanisms.

**E. Checkpoints, Lineage, and Time Travel ❌ Incorrect**

These provide:

- streaming reliability

- governance visibility

- historical data access

They do not enforce access control.

**Why B is correct**

A robust Unity Catalog security strategy combines three complementary layers:

- **Object-Level Security** determines **whether a user can access an object** (catalog, schema, table, view, etc.).

- **Row-Level Security** determines **which rows within the table** the user is allowed to see.

- **Column-Level Masking** determines **whether sensitive column values should be displayed or masked**.

Together, these features allow organizations to enforce the principle of least privilege while sharing a single copy of the data. Different users can access the same table yet see different rows and different column values based on their permissions, roles, or group memberships.

# [README](./../../../README.md)
