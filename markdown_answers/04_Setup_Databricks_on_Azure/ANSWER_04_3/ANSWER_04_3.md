# ANSWER 04 3

**Question 3**

**Which permission level is required to create an Azure Databricks workspace?**

**A. Reader ❌**

- **Why it's wrong:**

  - Reader permissions only allow viewing Azure resources.

  - Readers cannot create new services.

**B. Storage Blob Contributor ❌**

- **Why it's wrong:**

  - This role manages Azure Storage.

  - It does not allow deployment of Azure resources.

**C. Contributor ✅ Correct**

- **Why it's correct:**

  - Contributor can:

    - Create resources

    - Modify resources

    - Delete resources

  - This permission is sufficient to deploy an Azure Databricks workspace.

**D. Owner of the Azure tenant only ❌**

- **Why it's wrong:**

  - Owners have sufficient permissions.

  - However, **Owner is not required**.

  - Contributor is enough.

**E. Billing Administrator ❌**

- **Why it's wrong:**

  - Billing Administrators manage subscriptions and invoices.

  - They cannot deploy Azure resources unless granted Contributor or Owner permissions.

**Key Concept**

**Contributor** is the minimum Azure role commonly required to create Azure Databricks workspaces.

# [README](./../../../README.md)
