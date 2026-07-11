# EXPLANATION 43 1

**Question 1**

**What is the primary purpose of Lakehouse Federation in Databricks?**

**Correct Answer:**\
**B. To query external data sources directly without moving the data into the Lakehouse**

**Why B is Correct**

Lakehouse Federation allows Databricks to access data **where it already exists** instead of copying it into Delta Lake.

For example, Databricks can query:

- PostgreSQL

- SQL Server

- Oracle

- Snowflake

- Amazon Redshift

- Google BigQuery

- MySQL

The SQL query is sent to the external system, and the results are returned to Databricks. This avoids creating duplicate copies of the data.

**Why the other choices are wrong**

- Lakehouse Federation does **not** migrate databases.

- It does **not** replace Unity Catalog.

- It is **not** an ETL or data ingestion tool.

- It does **not** convert external databases into Delta tables automatically.

**Memory Tip**

**Federation = Query where the data lives.**

**Individual YouTube Video**

https://www.youtube.com/watch?v=mdw5j0l7K2Y

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Lakehouse+Federation+overview

------------------------------------------------------------------------

# [README](./../../../README.md)
