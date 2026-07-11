# EXPLANATION 48 10

**Question 10**

**Which tools are highlighted as part of the future CI/CD deployment workflow for Databricks projects?**

**Correct Answer:**\
**A. Azure Pipelines, Databricks Asset Bundles (DABs), and Databricks CLI**

**Why A is Correct**

A modern Databricks CI/CD workflow often looks like this:

Developer

↓

Git Folder

↓

Azure DevOps Repos

↓

Pull Request

↓

Azure Pipelines

↓

Databricks Asset Bundles (DABs)

↓

Databricks CLI

↓

Development

↓

Test

↓

Production

These tools work together:

- **Azure Pipelines** automates builds, tests, and deployments.

- **Databricks Asset Bundles (DABs)** define Databricks resources as code.

- **Databricks CLI** automates deployment and workspace management.

This combination is a recommended approach for production-grade Databricks deployments.

**Why the other choices are wrong**

Alternatives that omit one of these tools or replace them with unrelated services do not describe the CI/CD workflow presented in the lesson.

**Memory Tip**

Remember the pipeline:

**Git → Azure Pipelines → DABs → Databricks CLI → Deploy**

Below is a detailed explanation of each question, why the correct answer is correct, why the other concepts are incorrect, and recommended YouTube resources. The explanations are based on the current Databricks Git Folders documentation (formerly called **Databricks Repos**). Databricks renamed **Repos** to **Git Folders** in 2026, but the functionality remains essentially the same.

**Recommended Overall Video**

<https://www.youtube.com/watch?v=W_eFavJIPKw>

**Official Documentation**

https://docs.databricks.com/repos/

# [README](./../../../README.md)
