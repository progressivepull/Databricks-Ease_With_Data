# ANSWER 43 4

**Question 4**

**Before querying an external database with Lakehouse Federation, what must be created first?**

**A. A Delta Live Tables pipeline** ❌ Incorrect

- DLT processes data pipelines.

- Federation does not require DLT.

**B. A Materialized View** ❌ Incorrect

- Materialized Views are optional and unrelated to establishing the connection.

**C. A Connection** ✅ Correct

- The Connection stores:

  - Server

  - Database

  - Authentication

  - Credentials

- Without a Connection, Databricks has no way to reach the external database.

Workflow:

Create Connection

│

▼

Create Foreign Catalog

│

▼

Query Tables

**D. A Streaming Table** ❌ Incorrect

- Streaming Tables are for incremental ingestion.

**E. A Delta Sharing Recipient** ❌ Incorrect

- Delta Sharing is a different feature for sharing Delta data.

**Key Concept**

**Connection comes first.**

# [README](./../../../README.md)
