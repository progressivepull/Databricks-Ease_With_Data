# EXPLANATION 04 10

**Question 10**

**What is the correct high-level sequence for deploying Azure Databricks?**

**Correct Answer:**\
✅ **Create Resource Group → Create Virtual Network → Deploy Workspace → Launch Workspace**

**Explanation**

A typical deployment follows this order:

Create Resource Group\
↓\
Create Virtual Network\
↓\
Deploy Azure Databricks Workspace\
↓\
Launch Workspace\
↓\
Create Compute Cluster\
↓\
Run Notebooks

Why this order?

1.  **Resource Group** – Container for all Azure resources.

2.  **Virtual Network** – Provides secure networking.

3.  **Workspace** – Deploys the Azure Databricks service.

4.  **Launch Workspace** – Opens the Databricks environment where you create clusters and begin development.

Microsoft's deployment guidance follows this general workflow.

**YouTube**

**Deploy Azure Databricks in Azure Portal (Step-by-Step)**

<https://www.youtube.com/playlist?list=PLNj2XeCNjFeosTuxZLjfYvnW4H1hsPH07>

**Official Databricks Platform Administration Playlist**

<https://www.youtube.com/playlist?list=PLeK0Tsm_E67TIi_3N-FjOgrpFxbXBlqnq>

# [README](./../../../README.md)
