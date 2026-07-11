# ANSWER 49 1

**Question 1**

**What is the primary purpose of the Databricks CLI (Command Line Interface)?**

**A. To replace Unity Catalog for data governance** ❌ Incorrect

- Unity Catalog manages:

  - Permissions

  - Catalogs

  - Schemas

  - Lineage

  - Governance

- The CLI is simply a **tool to interact with Databricks**, not a governance system.

**B. To manage Databricks accounts and workspaces using terminal commands** ✅ Correct

- This is exactly what the Databricks CLI does.

- Instead of clicking through the Databricks UI, you can use terminal commands to manage resources.

Examples:

- List catalogs

- Create jobs

- Upload workspace files

- Deploy Asset Bundles

- Manage clusters

- Manage groups

- Manage Unity Catalog

Example:

databricks catalogs list

Instead of opening the UI.

Workflow:

Terminal

│

Databricks CLI

│

REST API

│

Databricks Workspace

**C. To automatically create SQL Warehouses** ❌ Incorrect

- The CLI **can** create SQL Warehouses through commands or automation.

- However, that is only **one capability**, not its primary purpose.

**D. To generate AI-powered dashboards** ❌ Incorrect

- AI/BI Dashboards and Genie provide analytics.

- The CLI does not generate dashboards.

**E. To convert notebooks into Delta tables** ❌ Incorrect

- Notebooks execute code.

- They are not converted into Delta tables.

**Key Concept**

**CLI = Command-line management tool for Databricks.**

# [README](./../../../README.md)
