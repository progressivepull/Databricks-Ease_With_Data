# ANSWER 41 1

**Question 1**

**What is the primary purpose of Databricks SQL (DBSQL)?**

**A. To create Spark clusters for ETL pipelines only** ❌ Incorrect

- ETL pipelines are primarily a **Data Engineering** task.

- While Spark clusters can run ETL jobs, **DBSQL is designed for analytics**, not cluster creation.

- Cluster management is separate from DBSQL.

**B. To provide a SQL analytics service for querying data, building reports, dashboards, and connecting BI tools** ✅ Correct

- This is exactly what Databricks SQL (DBSQL) is built for.

- It enables users to:

  - Write ANSI SQL queries

  - Analyze Delta tables

  - Build reports

  - Create dashboards

  - Connect BI tools like Power BI and Tableau

  - Perform OLAP (analytical) workloads

**C. To manage Unity Catalog permissions exclusively** ❌ Incorrect

- Unity Catalog handles:

  - Access control

  - Permissions

  - Catalogs

  - Schemas

  - Data governance

- DBSQL **uses** Unity Catalog but does not replace it.

**D. To replace Delta Lake storage** ❌ Incorrect

- Delta Lake is the storage layer.

- DBSQL is the analytics layer.

- DBSQL queries Delta tables; it doesn't replace them.

**E. To automate machine learning model training** ❌ Incorrect

- Machine Learning is handled through Databricks ML and MLflow.

- DBSQL focuses on SQL analytics.

**Key Concept**

**DBSQL = SQL Analytics Service**

Think:

- Query Data

- Analyze Data

- Build Dashboards

- Connect BI Tools

# [README](./../../../README.md)
