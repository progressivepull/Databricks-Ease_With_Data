# ANSWER 42 3

**Question 3**

**What is the primary purpose of a Materialized View?**

**A. To continuously ingest streaming files into Delta tables** ❌ Incorrect

- That's a Streaming Table.

**B. To replace Unity Catalog permissions** ❌ Incorrect

- Permissions remain managed by Unity Catalog.

**C. To store precomputed query results for faster analytics** ✅ Correct

- Materialized Views:

  - Execute expensive queries once.

  - Store the results.

  - Serve those stored results to future users.

- This avoids repeating costly calculations.

Example:

Without Materialized View

Dashboard

│

Complex Query

│

Millions of Rows

With Materialized View

Dashboard

│

Materialized View

(Precomputed Results)

**D. To automatically create SQL Warehouses** ❌ Incorrect

- SQL Warehouses must already exist.

**E. To manage Spark cluster configurations** ❌ Incorrect

- Cluster configuration is unrelated.

**Key Concept**

**Materialized View = Cached query results for faster analytics**

# [README](./../../../README.md)
