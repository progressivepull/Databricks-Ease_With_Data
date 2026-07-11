# EXPLANATION 44 3

**Question 3**

**Every Databricks SQL Alert is based on which of the following?**

**Correct Answer:**\
**C. A saved SQL query**

**Why C is Correct**

An alert needs a SQL query to evaluate.

Typical workflow:

Write SQL Query

↓

Save Query

↓

Create Alert

↓

Define Threshold

↓

Schedule Runs

The saved query provides the result that the alert evaluates. (In the latest alert experience, the query is owned by the alert, while legacy alerts referenced a saved query. Many training courses still teach the legacy model.)

**Why the other choices are wrong**

An alert is not based on:

- a dashboard

- a notebook

- a Delta table alone

- a job

**Memory Tip**

**No Query = No Alert**

**Individual YouTube Video**

https://www.youtube.com/watch?v=Itz0b6kQK9A

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+saved+query+alerts

------------------------------------------------------------------------

# [README](./../../../README.md)
