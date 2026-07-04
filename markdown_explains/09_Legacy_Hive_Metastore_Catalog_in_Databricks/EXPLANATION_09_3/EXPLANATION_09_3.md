# EXPLANATION 09 3

**Question 3**

**If no schema is specified when creating a table in the Hive Metastore, where is the table created?**

**Correct Answer:**\
✅ **Default schema**

**Explanation**

Hive Metastore automatically uses the **default** schema when no schema is specified.

Example:

CREATE TABLE employees (...)

actually becomes:

CREATE TABLE default.employees (...)

unless another schema has been selected.

The **default** schema serves as the standard location for tables when no schema is explicitly chosen.

**Example**

Hive Metastore\
\
↓\
\
default\
\
↓\
\
employees

**YouTube**

**Databricks Hive Metastore Tutorial**

https://www.youtube.com/results?search_query=Databricks+Hive+Metastore

# [README](./../../../README.md)
