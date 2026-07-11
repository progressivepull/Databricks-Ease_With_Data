# ANSWER 42 10

**Question 10**

**According to best practices, what is the correct refresh order when using both Streaming Tables and Materialized Views?**

**A. Refresh the Materialized View first, then the Streaming Table.** ❌ Incorrect

- The Materialized View would use stale data because the Streaming Table has not yet ingested the latest changes.

**B. Refresh both simultaneously.** ❌ Incorrect

- This can create timing issues where the Materialized View refreshes before new data is available.

**C. Refresh the Streaming Table first, then refresh the Materialized View.** ✅ Correct

- This ensures the Materialized View is built using the most recent streamed data.

Correct flow:

New Files

│

▼

Streaming Table Refresh

│

Latest Data Available

│

▼

Materialized View Refresh

│

Updated Dashboard

**D. Only refresh the Materialized View because the Streaming Table refreshes automatically.** ❌ Incorrect

- Depending on your workflow and configuration, you may still need to explicitly refresh the Streaming Table before refreshing downstream objects.

**E. Perform a full refresh of both every time.** ❌ Incorrect

- Full refreshes are much more expensive and are unnecessary for routine updates. Incremental refreshes are the recommended approach.

**Key Concept**

**Refresh upstream before downstream: Streaming Table first, Materialized View second.**

**Final Exam Summary**

| **Topic** | **Remember** |
|----|----|
| **Streaming Table** | Continuously ingests incremental data from streaming sources. |
| **Materialized View** | Stores precomputed query results for faster analytics and dashboards. |
| **Behind-the-scenes engine** | Delta Live Tables (DLT) manages refreshes and incremental processing. |
| **Required compute** | A SQL Warehouse is required to create and query Streaming Tables and Materialized Views in DBSQL. |
| **READ_FILES()** | Reads files (CSV, JSON, Parquet, etc.) directly from Unity Catalog Volumes or cloud storage. |
| **includeExistingFiles = false** | Skips previously existing files and processes only newly arriving files. |
| **Incremental vs. Full Refresh** | REFRESH STREAMING TABLE processes only new data; REFRESH STREAMING TABLE FULL reloads all source data. |
| **Materialized View optimization** | Uses stored query results to avoid recalculating expensive aggregations. |
| **NO OP optimization** | If no source data has changed, Databricks skips the refresh to save compute. |
| **Best refresh order** | Refresh the **Streaming Table first**, then refresh the **Materialized View** so reports use the latest data. |

# [README](./../../../README.md)
