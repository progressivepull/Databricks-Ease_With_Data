# ANSWER 42 8

**Question 8**

**Why do Materialized Views improve dashboard and reporting performance?**

**A. They automatically create Spark clusters.** ❌ Incorrect

- Cluster creation is unrelated.

**B. They eliminate the need for SQL Warehouses.** ❌ Incorrect

- SQL Warehouses still execute queries.

**C. They store precomputed query results instead of recomputing expensive aggregations each time.** ✅ Correct

- Instead of repeatedly calculating:

GROUP BY

SUM()

AVG()

COUNT()

Databricks stores the results.

Dashboard queries become much faster.

**D. They continuously ingest streaming files into Delta tables.** ❌ Incorrect

- That's a Streaming Table.

**E. They duplicate all source tables in memory.** ❌ Incorrect

- Materialized Views store query results, not entire tables in memory.

**Key Concept**

**Materialized View = Faster dashboards because expensive work is done ahead of time.**

# [README](./../../../README.md)
