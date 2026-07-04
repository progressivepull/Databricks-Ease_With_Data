# EXPLANATION 14 5

**Question 5**

**What is the primary characteristic of a temporary view?**

**Correct Answer:**\
✅ **It exists only during the current compute session.**

**Explanation**

Temporary Views exist **only while the Spark session is running**.

Example:

df.createOrReplaceTempView("employees")

Cluster Running\
\
↓\
\
View Exists\
\
↓\
\
Cluster Stops\
\
↓\
\
View Disappears

Temporary Views are commonly used for:

- Data exploration

- Intermediate transformations

- Temporary joins

They are **not stored permanently**.

**YouTube**

**Temporary Views in Databricks**

https://www.youtube.com/results?search_query=Databricks+Temporary+Views

# [README](./../../../README.md)
