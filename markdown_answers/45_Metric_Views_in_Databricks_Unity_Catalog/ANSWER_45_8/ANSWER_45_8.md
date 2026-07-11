# ANSWER 45 8

**Question 8**

**Why are joins included in Metric Views?**

**A. To replace SQL Warehouses with Delta Live Tables** ❌ Incorrect

- Different services.

**B. To automatically create Materialized Views** ❌ Incorrect

- Metric Views don't create Materialized Views.

**C. To expose additional business dimensions, such as customer information, without requiring users to write joins themselves** ✅ Correct

Example

Normally:

Orders

JOIN Customers

JOIN Products

JOIN Regions

Every dashboard repeats these joins.

Metric View

Orders

│

Customers

│

Products

│

Metric View

Dashboard developers simply query:

SELECT

customer_name,

measure(total_sales)

No joins required.

Benefits:

- Simpler SQL

- Fewer errors

- Consistent joins

**D. To convert relational databases into Delta tables** ❌ Incorrect

- Unrelated.

**E. To enable notebook scheduling** ❌ Incorrect

- Scheduling uses Workflows.

**Key Concept**

**Metric Views hide complex joins from dashboard developers.**

------------------------------------------------------------------------

# [README](./../../../README.md)
