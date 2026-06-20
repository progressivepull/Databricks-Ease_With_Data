# ANSWER 01 4

**What is the primary purpose of Unity Catalog in the Databricks ecosystem?**

A. To manage real-time streaming data ingestion pipelines\
**B. To provide a unified governance layer for data and AI assets across workspaces**\
C. To optimize cluster performance and resource allocation\
D. To replace Apache Spark as the main data processing engine\
E. To create interactive dashboards for business intelligence

**Correct Answer:** B

------------------------------------------------------------------------

Let’s break down each option so you clearly understand **why it’s correct or incorrect**.

**✅ Correct Answer: B**

**“To provide a unified governance layer for data and AI assets across workspaces”**

This is exactly what **Unity Catalog** does:

- Centralizes **data governance** (permissions, access control)

- Works across multiple **Databricks workspaces**

- Manages:

  - Tables

  - Files

  - Models

- Provides features like:

  - Data lineage

  - Auditing

  - Fine-grained access control

👉 In short: **one place to secure and manage all data + AI assets**

------------------------------------------------------------------------

**❌ A. To manage real-time streaming data ingestion pipelines**

**Why wrong:**

- This is handled by tools like:

  - **Apache Spark Structured Streaming**

  - **Delta Live Tables**

- Unity Catalog does **not manage pipelines**

👉 It governs data, not ingestion

------------------------------------------------------------------------

**❌ C. To optimize cluster performance and resource allocation**

**Why wrong:**

- Cluster performance is managed by:

  - Databricks compute settings

  - Spark configurations

- Unity Catalog is **not a performance tool**

👉 It focuses on governance, not compute optimization

------------------------------------------------------------------------

**❌ D. To replace Apache Spark as the main data processing engine**

**Why wrong:**

- Unity Catalog does **not process data**

- Apache Spark is still the **core processing engine**

- Unity Catalog works **on top of Spark**

👉 Governance layer ≠ processing engine

------------------------------------------------------------------------

**❌ E. To create interactive dashboards for business intelligence**

**Why wrong:**

- Dashboards are created using:

  - **Databricks SQL**

  - Tools like **Power BI, Tableau**

- Unity Catalog does **not handle visualization**

👉 It manages access to data used in dashboards

------------------------------------------------------------------------

**🔑 Simple Summary**

- **Unity Catalog = Governance + Security + Organization**

- Not for:

  - Processing ❌

  - Visualization ❌

  - Performance tuning ❌

👉 That’s why **B is correct**

# [README](./../../../README.md)
