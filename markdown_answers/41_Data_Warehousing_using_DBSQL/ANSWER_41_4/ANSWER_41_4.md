# ANSWER 41 4

**Question 4**

**Which optimization technology is used by Serverless SQL Warehouses to accelerate SQL query execution?**

**A. Delta Cache** ❌ Incorrect

- Delta Cache caches frequently read data.

- It is not the primary engine accelerating SQL execution.

**B. Photon Engine** ✅ Correct

- Photon is Databricks' high-performance vectorized query engine.

- It accelerates:

  - Filters

  - Joins

  - Aggregations

  - Sorting

  - SQL execution

It is written in C++ and optimized for modern CPUs.

**C. Auto Loader** ❌ Incorrect

- Auto Loader ingests files.

- It has nothing to do with SQL execution.

**D. MLflow Engine** ❌ Incorrect

- MLflow manages machine learning lifecycle.

**E. RocksDB** ❌ Incorrect

- RocksDB is used internally in some streaming/stateful workloads.

- It is unrelated to SQL Warehouse optimization.

**Key Concept**

**Photon = Faster SQL**

# [README](./../../../README.md)
