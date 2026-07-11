# EXPLANATION 44 4

**Question 4**

**Which component executes the SQL query used by a Databricks SQL Alert?**

**Correct Answer:**\
**B. SQL Warehouse attached to the saved query**

**Why B is Correct**

SQL Alerts require compute.

The compute is a **SQL Warehouse**, which:

- Executes the SQL query.

- Returns the results.

- Allows the alert condition to be evaluated.

Without a SQL Warehouse, the alert cannot run.

**Why the other choices are wrong**

- Unity Catalog manages metadata.

- Photon accelerates execution but is not the compute resource itself.

- Delta Lake stores data but does not execute queries.

**Memory Tip**

**Alert → SQL Warehouse → Query Runs**

**Individual YouTube Video**

[https://www.youtube.com/watch?v=zi3RCZVsQDs](https://www.youtube.com/watch?v=zi3RCZVsQDs&utm_source=chatgpt.com)

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+SQL+Warehouse

------------------------------------------------------------------------

# [README](./../../../README.md)
