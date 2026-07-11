# ANSWER 44 4

**Question 4**

**Which component executes the SQL query used by a Databricks SQL Alert?**

**A. Unity Catalog** ❌ Incorrect

- Unity Catalog manages:

  - Metadata

  - Permissions

  - Governance

- It does not execute SQL.

**B. SQL Warehouse attached to the saved query** ✅ Correct

- SQL Warehouses execute SQL.

- The alert simply tells the SQL Warehouse when to run the query.

Example:

Alert

│

Saved Query

│

SQL Warehouse

│

Results

**C. Delta Live Tables pipeline** ❌ Incorrect

- DLT processes pipelines.

**D. Databricks Repos** ❌ Incorrect

- Repos manage source code.

**E. MLflow Tracking Server** ❌ Incorrect

- MLflow tracks machine learning experiments.

**Key Concept**

**SQL Warehouse executes the query.**

# [README](./../../../README.md)
