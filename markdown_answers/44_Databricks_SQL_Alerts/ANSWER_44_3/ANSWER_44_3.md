# ANSWER 44 3

**Question 3**

**Every Databricks SQL Alert is based on which of the following?**

**A. A Delta Live Tables pipeline** ❌ Incorrect

- DLT pipelines process data.

- Alerts monitor query results.

**B. A Streaming Table** ❌ Incorrect

- Alerts can query Streaming Tables, but they are not built on them.

**C. A saved SQL query** ✅ Correct

- Every SQL Alert starts with a saved query.

Workflow:

Write SQL

│

Save Query

│

Create Alert

│

Choose Condition

│

Schedule Evaluation

**D. A Python notebook** ❌ Incorrect

- Alerts operate on saved SQL queries.

**E. A Unity Catalog Volume** ❌ Incorrect

- Volumes store files.

**Key Concept**

**No saved SQL query = No SQL Alert.**

# [README](./../../../README.md)
