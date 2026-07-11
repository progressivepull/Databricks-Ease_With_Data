# ANSWER 42 2

**Question 2**

**Although Streaming Tables and Materialized Views are created using SQL in DBSQL, what technology manages refreshes and incremental processing behind the scenes?**

**A. Apache Airflow** ❌ Incorrect

- Airflow schedules workflows.

- It does not manage Streaming Tables internally.

**B. Databricks Workflows** ❌ Incorrect

- Workflows schedule jobs.

- They do not provide the incremental refresh engine.

**C. Delta Live Tables (DLT)** ✅ Correct

- DLT powers:

  - Incremental processing

  - Dependency management

  - Refresh logic

  - Data quality features

- Even though users write SQL, DLT performs the processing behind the scenes.

**D. Apache Hive** ❌ Incorrect

- Hive is an older SQL warehouse technology.

- It isn't responsible for Streaming Table refreshes.

**E. Unity Catalog** ❌ Incorrect

- Unity Catalog provides governance and permissions.

- It does not perform data refreshes.

**Key Concept**

User writes SQL

│

▼

Streaming Table / Materialized View

│

Managed by

▼

Delta Live Tables (DLT)

# [README](./../../../README.md)
