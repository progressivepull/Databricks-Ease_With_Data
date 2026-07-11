# ANSWER 35 1

**Question 1**

**What is true about functions registered in Unity Catalog?**

**A. They exist only for the current Spark session. ❌ Incorrect**

- This describes a **PySpark session UDF**, not a Unity Catalog function.

- Session UDFs disappear when:

  - the notebook ends

  - the Spark session stops

  - the cluster restarts

Example:

spark.udf.register("tax_udf", tax_function)

This function exists only during the current session.

------------------------------------------------------------------------

**B. They cannot be shared between users. ❌ Incorrect**

- One of the biggest advantages of Unity Catalog functions is that they **can be shared**.

- If another user has permission, they can call the same function from another notebook or SQL query.

------------------------------------------------------------------------

**C. They are securable objects that can be shared, managed, and granted permissions. ✅ Correct**

Functions in Unity Catalog are **first-class securable objects**, just like:

- Tables

- Views

- Volumes

- Models

You can:

- GRANT EXECUTE

- REVOKE permissions

- View ownership

- Audit usage

- Manage them centrally

Example:

Metastore

↓

Catalog

↓

Schema

↓

Function

The function becomes part of your governed data platform.

------------------------------------------------------------------------

**D. They can only be used in SQL notebooks. ❌ Incorrect**

They can be used from:

- SQL

- PySpark

- Databricks notebooks

- Workflows

PySpark simply calls them differently.

------------------------------------------------------------------------

**E. They are stored inside Delta tables. ❌ Incorrect**

Functions are metadata objects.

Delta tables store **data**, not executable functions.

------------------------------------------------------------------------

**Why C is correct**

Unity Catalog functions are permanent, governed, and securable database objects that can be shared across users and workloads.

------------------------------------------------------------------------

# [README](./../../../README.md)
