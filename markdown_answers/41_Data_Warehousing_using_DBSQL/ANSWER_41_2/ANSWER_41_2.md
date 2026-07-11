# ANSWER 41 2

**Question 2**

**What is the role of a SQL Warehouse in Databricks?**

**A. It stores Delta Lake tables permanently.** ❌ Incorrect

- Delta tables are stored in cloud storage:

  - ADLS

  - Amazon S3

  - Google Cloud Storage

- SQL Warehouses are compute, not storage.

**B. It manages Unity Catalog permissions.** ❌ Incorrect

- Unity Catalog manages permissions.

- SQL Warehouses simply execute authorized queries.

**C. It serves as the compute engine that executes SQL queries.** ✅ Correct

- SQL Warehouse is the SQL compute engine.

- It:

  - Executes SQL

  - Processes joins

  - Aggregates data

  - Returns results

Think of it as:

SQL Query

↓

SQL Warehouse (Compute)

↓

Delta Tables

↓

Results

**D. It automatically creates dashboards from SQL queries.** ❌ Incorrect

- Dashboards are created by users.

- SQL Warehouse only runs the queries.

**E. It replaces the Databricks Control Plane.** ❌ Incorrect

- The Control Plane still manages the platform.

- SQL Warehouses are compute resources.

**Key Concept**

**SQL Warehouse = Compute for SQL**

# [README](./../../../README.md)
