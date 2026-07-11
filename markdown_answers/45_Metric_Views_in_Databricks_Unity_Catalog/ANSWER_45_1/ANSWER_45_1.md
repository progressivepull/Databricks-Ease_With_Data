# ANSWER 45 1

**Question 1**

**What is the primary purpose of a Metric View in Databricks Unity Catalog?**

**A. To automatically ingest streaming data into Delta tables** ❌ Incorrect

- This describes **Streaming Tables** or **Auto Loader**.

- Metric Views do **not** ingest data.

- They sit on top of existing tables and define business logic.

**B. To provide a centralized, reusable, governed semantic layer for business metrics and dimensions** ✅ Correct

- This is exactly what Metric Views are designed for.

- They create a **semantic layer**, meaning business definitions are stored once and reused everywhere.

- Instead of every report calculating revenue differently, everyone uses the same Metric View.

Example:

Without Metric Views

Dashboard A

Revenue = SUM(price)

Dashboard B

Revenue = SUM(price \* quantity)

Dashboard C

Revenue = Different SQL

Everyone gets different answers.

With Metric Views

Metric View

Revenue = Official Definition

Dashboard A

│

Dashboard B

│

Dashboard C

Everyone gets the same KPI.

**C. To replace SQL Warehouses for analytics** ❌ Incorrect

- SQL Warehouses execute SQL.

- Metric Views define reusable business logic.

- They work **together**.

**D. To create Delta Live Tables pipelines automatically** ❌ Incorrect

- DLT creates data pipelines.

- Metric Views don't create pipelines.

**E. To manage cluster configurations and autoscaling** ❌ Incorrect

- Cluster management is unrelated.

**Key Concept**

**Metric View = Semantic Layer for Business Metrics**

------------------------------------------------------------------------

# [README](./../../../README.md)
