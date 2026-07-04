# EXPLANATION 14 3

**Question 3**

**What is the primary benefit of using CREATE TABLE IF NOT EXISTS?**

**Correct Answer:**\
✅ **It avoids errors if the table already exists.**

**Explanation**

Normally:

CREATE TABLE employees (...)

If the table already exists:

ERROR

Instead:

CREATE TABLE IF NOT EXISTS employees (...);

Result:

Table Exists\
\
↓\
\
No Error\
\
↓\
\
Continue

This is especially useful for:

- ETL pipelines

- Automation

- Scheduled jobs

- Deployment scripts

You can safely run the script multiple times without failing.

**YouTube**

**Databricks SQL CREATE TABLE**

https://www.youtube.com/results?search_query=Databricks+CREATE+TABLE+IF+NOT+EXISTS

# [README](./../../../README.md)
