# 42 Streaming Tables and Materialized Views in DBSQL

**Streaming Tables and Materialized Views in Databricks SQL (DBSQL)**

This lesson explains how to create **Streaming Tables** and **Materialized Views** directly in **Databricks SQL (DBSQL)**. Although they are created using SQL syntax, Databricks still uses **Delta Live Tables (DLT)** behind the scenes to manage refreshes, incremental processing, and pipeline execution. The lesson demonstrates creating, refreshing, scheduling, and monitoring both object types.

------------------------------------------------------------------------

**1. Streaming Tables and Materialized Views in DBSQL**

Databricks SQL allows users to create:

- Streaming Tables

- Materialized Views

using SQL statements instead of Python-based DLT pipelines.

Even though the syntax is SQL, the backend implementation is still powered by **Delta Live Tables (DLT)**.

------------------------------------------------------------------------

**2. Streaming Tables**

A Streaming Table continuously ingests incremental data from a streaming source.

Example workflow:

CSV Files\
\
↓\
\
Streaming Source\
\
↓\
\
Streaming Table\
\
↓\
\
Incremental Data

Streaming Tables are designed for:

- Incremental file ingestion

- Streaming workloads

- Continuous updates

------------------------------------------------------------------------

**3. Materialized Views**

Materialized Views store **precomputed query results**.

Instead of rerunning expensive queries every time:

Source Table\
\
↓\
\
Aggregation\
\
↓\
\
Materialized View\
\
↓\
\
Fast Query

Users query the stored results instead of recomputing the aggregation.

------------------------------------------------------------------------

**4. SQL Warehouse Requirement**

Streaming Tables and Materialized Views created in DBSQL require a **SQL Warehouse**.

Workflow:

Notebook\
\
↓\
\
SQL Warehouse\
\
↓\
\
SQL Commands\
\
↓\
\
Streaming Table / Materialized View

A SQL Warehouse provides the execution engine for these SQL operations.

------------------------------------------------------------------------

**5. Reading Files with READ_FILES**

The lesson demonstrates reading CSV files stored in a Unity Catalog Volume.

Example workflow:

Volume\
\
↓\
\
READ_FILES()\
\
↓\
\
Streaming Source

READ_FILES() can also read from:

- Unity Catalog Volumes

- Azure Data Lake Storage (ADLS)

- Amazon S3

- Google Cloud Storage

------------------------------------------------------------------------

**6. Creating a Streaming Table**

Streaming Tables are created using SQL.

Conceptually:

CREATE OR REFRESH STREAMING TABLE\
\
↓\
\
READ_FILES()\
\
↓\
\
Streaming Table

The source must be a **streaming source**, which is why the query uses STREAM READ_FILES().

------------------------------------------------------------------------

**7. Incremental File Processing**

Initially:

Orders.csv\
\
↓\
\
Streaming Table\
\
↓\
\
14 Rows

After uploading another file:

Orders2.csv\
\
↓\
\
Refresh\
\
↓\
\
38 Rows

Only the newly added file is processed, demonstrating incremental ingestion.

**8. includeExistingFiles**

A key option demonstrated is:

includeExistingFiles = false

Behavior:

- Existing files are ignored after initial processing.

- Only newly arriving files are processed.

Without this option, previously processed files would be read again.

------------------------------------------------------------------------

**9. Refreshing Streaming Tables**

Streaming Tables support refresh operations.

Two modes are shown:

**Incremental Refresh**

REFRESH STREAMING TABLE

Processes only new data.

------------------------------------------------------------------------

**Full Refresh**

REFRESH STREAMING TABLE FULL

Reloads all data from the source.

------------------------------------------------------------------------

**10. DLT Behind the Scenes**

Although users issue SQL commands, Databricks automatically creates a DLT pipeline.

Workflow:

SQL Command\
\
↓\
\
DLT Pipeline\
\
↓\
\
Streaming Table

Query History shows an automatically generated DLT refresh operation after the SQL command executes.

------------------------------------------------------------------------

**11. Pipeline Metadata**

Running:

DESCRIBE EXTENDED

on a Streaming Table reveals metadata including:

- Table type

- Properties

- Pipeline ID

The Pipeline ID matches the automatically generated DLT pipeline that manages the table.

------------------------------------------------------------------------

**12. Creating a Materialized View**

Materialized Views are created from SQL queries.

Example:

Streaming Table\
\
↓\
\
GROUP BY\
\
↓\
\
SUM()\
\
↓\
\
Materialized View

The lesson aggregates order totals by order status.

------------------------------------------------------------------------

**13. Benefits of Materialized Views**

Instead of executing:

GROUP BY\
\
SUM\
\
COUNT

every time a query runs, the aggregated results are stored.

Benefits include:

- Faster queries

- Reduced compute

- Lower latency

- Better dashboard performance

------------------------------------------------------------------------

**14. Refreshing Materialized Views**

Materialized Views are refreshed separately.

Workflow:

Streaming Table\
\
↓\
\
Refresh Materialized View\
\
↓\
\
Updated Aggregations

The lesson refreshes the Streaming Table first, then refreshes the Materialized View so new aggregates become available.

------------------------------------------------------------------------

**15. Incremental Aggregation**

One of the most important concepts demonstrated is that Materialized Views **do not always recompute everything**.

Instead of:

Read Entire Table\
\
↓\
\
Recompute Everything

Databricks performs:

Read Incremental Data\
\
↓\
\
Incremental Aggregation

This significantly improves refresh performance.

------------------------------------------------------------------------

**16. DLT Planning Strategies**

The DLT pipeline uses different execution strategies.

Examples include:

**Group Aggregate**

Group Aggregate\
\
↓\
\
Incremental Processing

Only new records are aggregated.

**Complete Recompute**

Complete Recompute\
\
↓\
\
Read Entire Dataset

Used only when necessary.

------------------------------------------------------------------------

**17. No-Op Optimization**

If no new data exists:

Refresh\
\
↓\
\
No New Files\
\
↓\
\
No Operation (NO OP)

Databricks skips unnecessary processing.

This saves:

- Compute

- Time

- Cost

No aggregation is rerun because nothing changed.

------------------------------------------------------------------------

**18. Monitoring with Query History**

Query History displays:

- SQL statements

- Refresh operations

- Automatically created DLT jobs

- Pipeline execution

Users can trace SQL commands back to the underlying DLT pipeline.

------------------------------------------------------------------------

**19. Scheduling Refreshes**

Both Streaming Tables and Materialized Views support scheduled refreshes.

Example:

SCHEDULE EVERY 4 HOURS

Databricks automatically refreshes:

- Streaming Tables

- Materialized Views

at the specified interval.

------------------------------------------------------------------------

**20. Cron Scheduling**

Instead of fixed intervals, refreshes can use cron expressions.

Example:

CRON expression\
\
↓\
\
Automatic Refresh

This enables complex scheduling such as:

- Daily

- Weekly

- Monthly

- Business hours

**Streaming Tables vs Materialized Views**

| **Feature**         | **Streaming Table**   | **Materialized View**         |
|---------------------|-----------------------|-------------------------------|
| Purpose             | Incremental ingestion | Precomputed query results     |
| Source              | Streaming data        | Tables or Streaming Tables    |
| Stores raw data     | Yes                   | No (stores computed results)  |
| Incremental refresh | Yes                   | Yes                           |
| Backend             | Delta Live Tables     | Delta Live Tables             |
| Typical use         | Data ingestion        | Fast analytics and dashboards |

------------------------------------------------------------------------

**DBSQL vs DLT Creation**

| **Feature**           | **DBSQL**         | **Traditional DLT** |
|-----------------------|-------------------|---------------------|
| Language              | SQL               | Python or SQL       |
| Backend               | Delta Live Tables | Delta Live Tables   |
| Pipeline creation     | Automatic         | Manual              |
| User manages pipeline | No                | Yes                 |
| Refresh               | SQL commands      | Pipeline execution  |

------------------------------------------------------------------------

**Best Practices**

- Use **Streaming Tables** for incremental ingestion of files from cloud storage or Unity Catalog Volumes.

- Set **includeExistingFiles = false** when you want to process only newly arriving files after the initial load.

- Use **Materialized Views** for expensive aggregations and reporting queries to improve dashboard and analytics performance.

- Refresh the **Streaming Table before refreshing the Materialized View** so new data is included in downstream aggregates.

- Monitor refresh operations in **Query History** to understand how the automatically managed DLT pipelines execute.

- Schedule refreshes using **fixed intervals** or **cron expressions** to keep Streaming Tables and Materialized Views synchronized without manual intervention.

# [README](./../../../README.md)
