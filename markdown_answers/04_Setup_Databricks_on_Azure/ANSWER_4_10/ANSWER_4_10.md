# ANSWER 4 10

**Question 10**

**What is the correct high-level sequence for deploying Azure Databricks?**

**A. Launch Workspace → Create VNet → Create Resource Group ❌**

- **Why it's wrong:**

  - The workspace cannot be launched before the required Azure infrastructure exists.

**B. Create Workspace → Create Resource Group → Configure Networking ❌**

- **Why it's wrong:**

  - A workspace must be deployed into an existing Resource Group and networking environment.

**C. Create Resource Group → Create Virtual Network → Deploy Workspace → Launch Workspace ✅ Correct**

- **Why it's correct:**

  - This follows the typical deployment workflow:

    1.  Create a Resource Group.

    2.  Create and configure the Virtual Network (and subnets, if using VNet injection).

    3.  Deploy the Azure Databricks workspace.

    4.  Launch and configure the workspace.

**D. Configure Unity Catalog → Create Workspace → Create Virtual Network ❌**

- **Why it's wrong:**

  - Unity Catalog is configured after the Databricks workspace and account infrastructure are available.

**E. Create Compute Cluster → Create Resource Group → Launch Workspace ❌**

- **Why it's wrong:**

  - Compute clusters are created inside an existing Databricks workspace, so they cannot come first.

**Key Concept**

A successful Azure Databricks deployment starts with the underlying Azure infrastructure (Resource Group and networking), then the workspace is created, and finally the workspace is launched and configured.

# [README](./../../../README.md)
