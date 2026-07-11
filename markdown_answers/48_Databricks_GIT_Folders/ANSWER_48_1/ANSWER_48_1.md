# ANSWER 48 1

**Question 1**

**What is the primary purpose of Databricks Git Folders?**

**A. To automatically create Delta Live Tables pipelines** ❌ Incorrect

- Delta Live Tables (DLT) is used to build and manage data pipelines.

- Git Folders do **not** create pipelines.

- Git Folders are for **source code management**.

**B. To integrate Git repositories with a Databricks workspace for version control and collaboration** ✅ Correct

- This is exactly what Git Folders are for.

- They connect your Databricks workspace to a Git repository (Azure DevOps, GitHub, GitLab, Bitbucket, etc.).

- Benefits include:

  - Version control

  - Collaboration

  - Branching

  - Pulling updates

  - Committing changes

  - Pushing code

Example:

Azure DevOps Repo

▲

│

Clone / Pull / Push

│

Databricks Git Folder

│

Notebooks

Python

SQL

YAML

**C. To replace Unity Catalog for data governance** ❌ Incorrect

- Unity Catalog manages:

  - Permissions

  - Governance

  - Lineage

- Git manages source code.

**D. To schedule SQL queries automatically** ❌ Incorrect

- SQL scheduling uses SQL Editor schedules or Workflows.

**E. To manage SQL Warehouse configurations** ❌ Incorrect

- SQL Warehouses are configured separately.

**Key Concept**

**Git Folders = Git inside Databricks.**

# [README](./../../../README.md)
