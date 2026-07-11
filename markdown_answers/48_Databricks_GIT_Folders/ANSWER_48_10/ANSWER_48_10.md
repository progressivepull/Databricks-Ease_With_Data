# ANSWER 48 10

**Question 10**

**Which tools are highlighted as part of the future CI/CD deployment workflow for Databricks projects?**

**A. Azure Pipelines, Databricks Asset Bundles (DABs), and Databricks CLI** ✅ Correct

These tools work together:

**Azure Pipelines**

Automates builds and deployments.

↓

**Databricks Asset Bundles (DABs)**

Packages Databricks resources:

- Jobs

- Pipelines

- Notebooks

- Resources

↓

**Databricks CLI**

Deploys resources into Databricks.

Workflow:

Git Repo

│

Azure Pipeline

│

Databricks Asset Bundle

│

Databricks CLI

│

Deploy Workspace

**B. Unity Catalog, Delta Sharing, and MLflow** ❌ Incorrect

- These are important Databricks services but not the primary CI/CD deployment tools.

**C. SQL Alerts, Genie Spaces, and Metric Views** ❌ Incorrect

- These are analytics features.

**D. Apache Hive, Apache NiFi, and Kafka** ❌ Incorrect

- These are unrelated technologies.

**E. Power BI, Tableau, and Excel** ❌ Incorrect

- These are reporting tools.

**Key Concept**

**Modern Databricks CI/CD = Azure Pipelines + DABs + Databricks CLI**

**Final Exam Summary**

| **Topic** | **Remember** |
|----|----|
| **Git Folders** | Integrate Git repositories with Databricks for version control and collaboration. |
| **Common Git Operations** | Clone, Pull, Commit, Push, Branch, and Merge. |
| **Azure DevOps Repos** | Git repository service that stores notebooks, source code, YAML, and configuration files. |
| **Authentication** | The lesson uses **Username + Personal Access Token (PAT)** to connect Databricks to Azure DevOps. |
| **Sparse Checkout** | Clones only selected folders from a repository to reduce download size and workspace clutter. |
| **Feature Branches** | Allow developers to work independently without affecting the main branch until changes are ready to merge. |
| **Source Format** | Saves notebooks as source files (for example, .py for Python), making Git diffs, code reviews, and merges much easier than the default notebook format. |
| **Modified Status** | **M (Modified)** indicates local changes that have not yet been committed. |
| **Typical Git Workflow** | Create/Edit → Commit → Push (after cloning the repository). |
| **Future CI/CD Stack** | **Azure Pipelines** automates deployments, **Databricks Asset Bundles (DABs)** package project resources, and the **Databricks CLI** deploys them into Databricks workspaces. |

# [README](./../../../README.md)
