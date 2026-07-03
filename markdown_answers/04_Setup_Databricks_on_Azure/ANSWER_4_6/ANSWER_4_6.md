# ANSWER 4 6

**Question 6**

**What is the primary purpose of an Azure Resource Group during Azure Databricks deployment?**

**A. To execute Spark jobs ❌**

- **Why it's wrong:**

  - Spark jobs run on compute clusters, not Resource Groups.

**B. To store Delta tables ❌**

- **Why it's wrong:**

  - Delta tables are stored in cloud storage such as Azure Data Lake Storage.

**C. To organize and manage related Azure resources together ✅ Correct**

- **Why it's correct:**

  - Resource Groups logically organize related resources, including:

    - Databricks workspace

    - Virtual Network

    - Network Security Groups

    - Storage

  - They simplify deployment, permissions, monitoring, and deletion.

**D. To replace Unity Catalog ❌**

- **Why it's wrong:**

  - Unity Catalog manages governance and metadata.

  - Resource Groups manage Azure resources.

**E. To provide authentication for Databricks users ❌**

- **Why it's wrong:**

  - Authentication is handled by Microsoft Entra ID (formerly Azure Active Directory), not Resource Groups.

**Key Concept**

A Resource Group is simply a **container that organizes Azure resources**.

# [README](./../../../README.md)
