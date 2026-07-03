# ANSWER 06 6

**Question 6**

**What does the following command create in a Databricks notebook?**

spark.range(0,10)

**A. A Delta table containing values 0–10** ❌ Incorrect

- No table is created.

- Nothing is written to storage.

**B. A Spark DataFrame containing values 0 through 9** ✅ **Correct**

- spark.range(start, end) creates a DataFrame with one column named id.

- The end value is **exclusive**, so the DataFrame contains:

| **id** |
|--------|
| 0      |
| 1      |
| 2      |
| 3      |
| 4      |
| 5      |
| 6      |
| 7      |
| 8      |
| 9      |

**C. A SQL database named Range** ❌ Incorrect

- No database is created.

**D. A Python list of numbers** ❌ Incorrect

- The result is a distributed Spark DataFrame, not a Python list.

**E. A new Spark cluster** ❌ Incorrect

- The command runs on an existing cluster.

- It does not create one.

**Key Concept**

spark.range() is a quick way to generate a Spark DataFrame for testing or demonstrations.

------------------------------------------------------------------------

# [README](./../../../README.md)
