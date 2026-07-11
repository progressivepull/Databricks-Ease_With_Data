# EXPLANATION 44 10

**Question 10**

**What is the difference between a Query Schedule and an Alert Schedule?**

**Correct Answer:**\
**C. The Query Schedule executes the saved query, while the Alert Schedule determines when the alert condition is evaluated.**

**Why C is Correct**

Although they are closely related, they serve different purposes:

- **Query Schedule:** Runs the SQL query to produce results.

- **Alert Schedule:** Determines when those results are evaluated against the alert condition and notifications are sent.

In many legacy Databricks SQL workflows, these schedules were configured separately; newer alert workflows integrate scheduling directly into the alert editor, but certification materials often still distinguish the two concepts.

**Why the other choices are wrong**

The schedules do not perform the same function:

- One is responsible for executing SQL.

- The other is responsible for evaluating thresholds and sending notifications.

**Memory Tip**

Query Schedule

↓

Runs SQL

Alert Schedule

↓

Checks Condition

If TRUE

↓

Send Notification

**Individual YouTube Video**

https://www.youtube.com/watch?v=Itz0b6kQK9A

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+SQL+Alerts+schedule

Below is a detailed explanation of each question, why the correct answer is correct, why the other concepts are incorrect, and recommended YouTube resources. The explanations are based on current Databricks SQL, Streaming Tables, Materialized Views, and Lakeflow Declarative Pipelines (formerly Delta Live Tables) documentation.

**Recommended overall video**

**Databricks SQL: Materialized Views & Streaming Tables**

YouTube Search:

https://www.youtube.com/results?search_query=Databricks+Streaming+Tables+Materialized+Views

Official Documentation:

https://docs.databricks.com/sql/

# [README](./../../../README.md)
