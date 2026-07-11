# ANSWER 41 7

**Question 7**

**Which information is typically required for a BI tool such as Power BI or Tableau to connect to a SQL Warehouse?**

**A. Notebook path and cluster ID** ❌ Incorrect

- BI tools don't connect to notebooks.

**B. Delta table location only** ❌ Incorrect

- BI tools connect to compute, not directly to storage.

**C. Hostname, HTTP Path, and JDBC URL** ✅ Correct

- These are the standard connection details:

  - Hostname

  - HTTP Path

  - JDBC/ODBC connection information

  - Authentication credentials (such as personal access token or OAuth, depending on configuration)

**D. Workspace ID and Spark version only** ❌ Incorrect

- Those are insufficient for a connection.

**E. Unity Catalog metastore ID only** ❌ Incorrect

- The metastore doesn't establish BI connectivity.

**Key Concept**

**BI Connection = Hostname + HTTP Path + JDBC/ODBC information**

# [README](./../../../README.md)
