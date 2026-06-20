# ANSWER 01 7

**What is the primary purpose of Jobs & Workflows in Databricks?**

A. To create interactive dashboards for business intelligence reporting\
**B. To manage and orchestrate automated execution of notebooks, scripts, and data pipelines**\
C. To replace Unity Catalog for centralized data governance\
D. To store unstructured data in a scalable cloud storage system\
E. To optimize GPU performance for machine learning model training

**Correct Answer:** B. To manage and orchestrate automated execution of notebooks, scripts, and data pipelines

------------------------------------------------------------------------

Let’s break down each option so you clearly understand **why it’s correct or incorrect**.

**✅ Correct Answer: B**

**“To manage and orchestrate automated execution of notebooks, scripts, and data pipelines”**

This is the main purpose of **Jobs & Workflows** in Databricks:

- Automates execution of:

  - Notebooks

  - Python scripts

  - SQL queries

  - DLT pipelines

- Supports:

  - Scheduling

  - Task dependencies

  - Monitoring

  - Retry handling

👉 It acts like a workflow orchestration system for data and AI tasks.

**❌ A. To create interactive dashboards for business intelligence reporting**

**Why wrong:**

- Dashboards are created using:

  - Databricks SQL

  - Power BI

  - Tableau

- Jobs & Workflows automates tasks, not visualizations.

👉 Workflow orchestration ≠ dashboard creation

------------------------------------------------------------------------

**❌ C. To replace Unity Catalog for centralized data governance**

**Why wrong:**

- Unity Catalog handles:

  - Permissions

  - Governance

  - Lineage

- Jobs & Workflows handles:

  - Task execution

  - Scheduling

  - Automation

👉 Different responsibilities

------------------------------------------------------------------------

**❌ D. To store unstructured data in a scalable cloud storage system**

**Why wrong:**

- Storage systems include:

  - AWS S3

  - Azure Data Lake Storage

  - Google Cloud Storage

- Jobs & Workflows does not store data.

👉 It orchestrates processes, not storage

------------------------------------------------------------------------

**❌ E. To optimize GPU performance for machine learning model training**

**Why wrong:**

- GPU optimization is handled by:

  - Compute configurations

  - Spark settings

  - ML frameworks

- Jobs & Workflows may schedule ML jobs, but it does not optimize hardware performance.

👉 Scheduling ML jobs ≠ hardware optimization

------------------------------------------------------------------------

**🔑 Simple Summary**

- **Jobs & Workflows = Automation + Scheduling + Orchestration**

- Used to:

  - Run notebooks automatically

  - Schedule pipelines

  - Manage dependencies

  - Monitor workflows

👉 That’s why **B is correct**

# [README](./../../../README.md)
