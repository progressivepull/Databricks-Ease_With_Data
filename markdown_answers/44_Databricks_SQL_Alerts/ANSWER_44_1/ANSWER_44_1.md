# ANSWER 44 1

**Question 1**

**What is the primary purpose of Databricks SQL Alerts?**

**A. To automatically optimize SQL queries for better performance** ❌ Incorrect

- SQL Alerts do **not** optimize queries.

- Query optimization is handled by technologies such as:

  - Photon Engine

  - Predictive I/O

  - Query Optimizer

- Alerts simply monitor query results.

**B. To continuously monitor SQL query results and send notifications when specified conditions are met** ✅ Correct

- This is exactly what SQL Alerts are designed for.

- Workflow:

  1.  Execute a saved SQL query.

  2.  Evaluate a condition.

  3.  Send a notification if the condition is true.

Example:

Saved Query

│

Runs on Schedule

│

Returns Value

│

Condition?

│

Yes ───► Send Alert

No ───► Do Nothing

**C. To automatically create Materialized Views from SQL queries** ❌ Incorrect

- Materialized Views are created explicitly using SQL.

- Alerts never create database objects.

**D. To replicate SQL query results into Delta Lake** ❌ Incorrect

- Alerts monitor results; they don't copy data.

**E. To schedule notebook execution in Databricks Workflows** ❌ Incorrect

- Notebook scheduling is handled by Databricks Workflows, not SQL Alerts.

**Key Concept**

**SQL Alerts = Monitor query results and notify when conditions are met.**

# [README](./../../../README.md)
