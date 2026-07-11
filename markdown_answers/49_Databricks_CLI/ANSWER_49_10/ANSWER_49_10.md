# ANSWER 49 10

**Question 10**

**What is the primary role of the Databricks CLI in relation to Databricks Asset Bundles (DABs)?**

**A. It converts notebooks into SQL queries automatically.** ❌ Incorrect

- The CLI does not convert notebooks into SQL.

**B. It serves as the primary interface for deploying notebooks, jobs, pipelines, and other Databricks assets across environments.** ✅ Correct

Typical deployment flow:

Git Repository

│

Azure Pipeline

│

Databricks CLI

│

Asset Bundle

│

DEV

TEST

PROD

The CLI is the tool that executes deployment commands, such as:

databricks bundle validate

databricks bundle deploy

It deploys:

- Notebooks

- Jobs

- Pipelines

- Resources

- Configuration

- Other Databricks assets

**C. It replaces Azure DevOps Pipelines for CI/CD.** ❌ Incorrect

- Azure Pipelines orchestrate CI/CD.

- The CLI performs Databricks-specific deployment tasks.

**D. It creates SQL Warehouses automatically during deployment.** ❌ Incorrect

- The CLI can create resources if instructed, but that is not its primary role in relation to DABs.

**E. It manages Unity Catalog permissions for all users.** ❌ Incorrect

- The CLI can manage permissions through commands, but DAB deployment is about deploying Databricks assets, not universally managing permissions.

**Key Concept**

**DABs define what to deploy; the Databricks CLI performs the deployment.**

**Final Exam Summary**

| **Topic** | **Remember** |
|----|----|
| **Databricks CLI** | Command-line tool for managing Databricks accounts and workspaces. |
| **Built On** | The Databricks **REST API**; the CLI is a user-friendly wrapper around API calls. |
| **Primary Benefit** | Enables automation, scripting, and CI/CD workflows. |
| **Verify Installation** | Run **databricks -v** to display the installed CLI version. |
| **Development Authentication** | **User-to-Machine (U2M)** is best for local, interactive development. |
| **Automation Authentication** | **Machine-to-Machine (M2M)** using a **Service Principal** is recommended for CI/CD and unattended deployments. |
| **Authentication Profiles** | Stored in the **.databricks.cfg** file. |
| **List Catalogs** | Use **databricks catalogs list** to view accessible Unity Catalog catalogs. |
| **Help Command** | Use **databricks --help** (or --help on subcommands) to see available commands and options. |
| **CLI + Databricks Asset Bundles (DABs)** | DABs describe the resources to deploy, and the **Databricks CLI** is the primary tool that validates and deploys notebooks, jobs, pipelines, and other Databricks assets across environments. |

# [README](./../../../README.md)
