# EXPLANATION 42 2

**Question 2**

**Although Streaming Tables and Materialized Views are created using SQL in DBSQL, what technology manages refreshes and incremental processing behind the scenes?**

**Correct Answer:**\
**C. Delta Live Tables (DLT)**

**Note:** Databricks has renamed Delta Live Tables to **Lakeflow Declarative Pipelines**. Many courses and certification materials still refer to it as **DLT**, so that remains the expected answer.

**Why C is Correct**

When you create a Streaming Table or Materialized View using SQL, Databricks automatically uses **Lakeflow Declarative Pipelines (formerly DLT)** behind the scenes to:

- Track dependencies

- Detect new data

- Perform incremental refreshes

- Recover from failures

- Optimize execution

Users simply write SQL while the pipeline infrastructure manages processing automatically.

**Why the other choices are wrong**

- SQL Warehouse executes SQL but does not orchestrate incremental refresh logic.

- Photon accelerates execution but is not the pipeline manager.

- Unity Catalog governs metadata and permissions.

**Memory Tip**

SQL writes the definition.

**DLT/Lakeflow runs it.**

**Individual YouTube Video**

Delta Live Tables Introduction

https://www.youtube.com/watch?v=WWM4Y8R7n8Q

**YouTube Search**

https://www.youtube.com/results?search_query=Delta+Live+Tables+Databricks

------------------------------------------------------------------------

# [README](./../../../README.md)
