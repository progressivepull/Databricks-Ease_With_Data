# ANSWER 47 1

**Question 1**

**What is the primary purpose of AI/BI Genie Spaces in Databricks?**

**A. To automatically create Delta Live Tables pipelines** ❌ Incorrect

- Delta Live Tables (DLT) is used for **building and managing data pipelines**.

- Genie does **not** create pipelines.

- Genie is focused on helping users **ask questions about data**, not moving or transforming data.

**B. To allow business users to query data using natural language instead of writing SQL** ✅ Correct

- This is exactly what AI/BI Genie is designed for.

- Instead of writing SQL like:

SELECT SUM(sales)

FROM orders

WHERE year = 2025;

A user can simply ask:

**"What were total sales in 2025?"**

Genie then:

1.  Understands the question.

2.  Generates SQL.

3.  Executes the SQL.

4.  Returns results.

Example:

Business User

│

"Show total sales for 2025"

│

▼

AI/BI Genie

│

Generates SQL

│

SQL Warehouse

│

Results + Chart

**C. To replace SQL Warehouses with Spark clusters** ❌ Incorrect

- Genie actually **uses SQL Warehouses** to run queries.

- It does not replace them.

**D. To automatically optimize Unity Catalog permissions** ❌ Incorrect

- Unity Catalog permissions are managed separately.

**E. To schedule notebook execution using Workflows** ❌ Incorrect

- Databricks Workflows schedules notebooks.

- Genie is for conversational analytics.

**Key Concept**

**Genie = Ask questions in English instead of SQL.**

# [README](./../../../README.md)
