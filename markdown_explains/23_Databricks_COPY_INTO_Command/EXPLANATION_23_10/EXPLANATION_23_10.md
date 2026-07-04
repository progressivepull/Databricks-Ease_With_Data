# EXPLANATION 23 10

**Question 9**

**Which feature of COPY INTO allows loading data into a table whose schema changes over time?**

**Correct Answer: B. Schema Evolution**

**Explanation**

**Schema Evolution** lets a table adapt when new columns appear in the source data.

Original CSV:

EmployeeID,Name

Later:

EmployeeID,Name,Department

With schema evolution enabled, Databricks can add the new Department column to the Delta table automatically.

Benefits:

- Supports evolving data sources.

- Reduces manual maintenance.

- Keeps ingestion pipelines resilient to change.

**YouTube**

- **Delta Lake Schema Evolution**\
  https://www.youtube.com/results?search_query=Delta+Lake+Schema+Evolution

# [README](./../../../README.md)
