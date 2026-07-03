# ANSWERS

**Question 1**

**Which cloud providers currently support Databricks deployments?**

**A. AWS, Oracle Cloud, IBM Cloud ❌**

- **Why it's wrong:** Oracle Cloud and IBM Cloud are **not officially supported Databricks deployment platforms**.

- AWS is correct, but the other two providers make the answer incorrect.

**B. AWS, Microsoft Azure, Google Cloud Platform (GCP) ✅ Correct**

- **Why it's correct:** Databricks is officially available on:

  - **Amazon Web Services (AWS)**

  - **Microsoft Azure**

  - **Google Cloud Platform (GCP)**

- These are the only three major cloud providers currently supported.

**C. Azure, VMware Cloud, Oracle Cloud ❌**

- **Why it's wrong:**

  - Azure is supported.

  - VMware Cloud and Oracle Cloud are not supported deployment platforms for Databricks.

- Since only one provider is correct, the answer is incorrect.

**D. Azure, DigitalOcean, IBM Cloud ❌**

- **Why it's wrong:**

  - Azure is supported.

  - DigitalOcean and IBM Cloud do not support Databricks deployments.

**E. AWS, Alibaba Cloud, Oracle Cloud ❌**

- **Why it's wrong:**

  - AWS is supported.

  - Alibaba Cloud and Oracle Cloud are not official Databricks deployment platforms.

**Key Concept**

Only **three cloud providers** officially host Databricks:

- AWS

- Microsoft Azure

- Google Cloud Platform (GCP)

**Question 2**

**Which Azure subscription type is required to deploy Azure Databricks?**

**A. Azure Free Trial subscription ❌**

- **Why it's wrong:**

  - A Free Trial is temporary and has limited credits.

  - It is not the standard subscription expected for long-term Azure Databricks deployments.

**B. Student subscription only ❌**

- **Why it's wrong:**

  - Azure for Students has limited capabilities and credits.

  - It is not the required subscription type.

**C. Enterprise Agreement only ❌**

- **Why it's wrong:**

  - Enterprise Agreements are one option for organizations.

  - They are **not required** to deploy Azure Databricks.

**D. Pay-As-You-Go subscription ✅ Correct**

- **Why it's correct:**

  - A Pay-As-You-Go subscription allows Azure to bill for:

    - Virtual Machines

    - Storage

    - Networking

    - Databricks services

  - This is the most common subscription used for Azure Databricks deployments.

**E. MSDN subscription only ❌**

- **Why it's wrong:**

  - MSDN subscriptions are developer benefits.

  - They are not required for Azure Databricks.

**Key Concept**

Azure Databricks requires an Azure subscription capable of creating and paying for Azure resources. The standard choice is **Pay-As-You-Go**.

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

**Question 4**

**Azure Databricks billing consists of which two primary cost categories?**

**A. Azure AD licensing and SQL licensing ❌**

- **Why it's wrong:**

  - Azure AD and SQL licensing are unrelated to Databricks compute costs.

**B. Databricks Units (DBUs) and Azure cloud resource charges ✅ Correct**

- **Why it's correct:**

  - You pay for:

    - **Databricks Units (DBUs)** for the Databricks platform.

    - **Azure resources**, including:

      - Virtual Machines

      - Storage

      - Networking

      - Managed Disks

**C. Virtual Network charges and Unity Catalog licensing ❌**

- **Why it's wrong:**

  - Networking costs are part of Azure charges.

  - Unity Catalog does not have a separate licensing model in this context.

**D. Workspace licensing and notebook execution fees ❌**

- **Why it's wrong:**

  - Databricks does not charge separately per notebook execution.

**E. Azure DevOps charges and storage licensing ❌**

- **Why it's wrong:**

  - Azure DevOps is unrelated to Databricks pricing.

**Key Concept**

Think of Databricks costs as:

**Total Cost = DBUs + Azure Infrastructure**

**Question 5**

**Why are two subnets created when deploying Azure Databricks?**

**A. One for SQL Warehouses and one for Unity Catalog ❌**

- **Why it's wrong:**

  - SQL Warehouses and Unity Catalog do not require dedicated subnets.

**B. One for storage and one for notebooks ❌**

- **Why it's wrong:**

  - Storage and notebooks are not separated by subnet.

**C. One public subnet and one private subnet for network separation and security ✅ Correct**

- **Why it's correct:**

  - Azure Databricks commonly uses:

    - Public subnet

    - Private subnet

  - This improves:

    - Security

    - Network isolation

    - Traffic control

**D. One subnet for developers and one for administrators ❌**

- **Why it's wrong:**

  - Azure networking is not organized by user roles.

**E. Azure requires exactly two subnets for every virtual network ❌**

- **Why it's wrong:**

  - Azure allows many subnet configurations.

  - The two-subnet design is specific to Databricks deployment recommendations, not an Azure requirement.

**Key Concept**

Two subnets improve **security and isolation**, not user organization.

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

**Question 7**

**Which deployment option provides access to additional enterprise features during the evaluation period?**

**A. Standard Tier ❌**

- **Why it's wrong:**

  - Standard Tier includes fewer enterprise capabilities.

**B. Community Edition ❌**

- **Why it's wrong:**

  - Community Edition is free but has significant limitations and lacks enterprise features.

**C. Premium 14-day Trial ✅ Correct**

- **Why it's correct:**

  - The Premium trial provides temporary access to enterprise capabilities such as advanced security and governance features for evaluation.

**D. Personal Workspace ❌**

- **Why it's wrong:**

  - A Personal Workspace is an individual user's workspace area, not a licensing tier.

**E. Serverless Trial ❌**

- **Why it's wrong:**

  - Serverless is a compute option, not the evaluation tier described in the question.

**Key Concept**

The **Premium 14-day Trial** lets users evaluate advanced enterprise features before purchasing.

**Question 8**

**During networking configuration for Azure Databricks, which setting is recommended?**

**A. Enable public IP addresses for all clusters ❌**

- **Why it's wrong:**

  - Public IPs increase the attack surface and are generally discouraged for secure enterprise deployments.

**B. Disable public IP addresses and use the custom Virtual Network ✅ Correct**

- **Why it's correct:**

  - Using a customer-managed Virtual Network with no public IPs improves:

    - Security

    - Compliance

    - Network control

**C. Use Azure's default Virtual Network without customization ❌**

- **Why it's wrong:**

  - While possible for simple setups, enterprise deployments typically use custom VNets to meet security and networking requirements.

**D. Skip Virtual Network configuration completely ❌**

- **Why it's wrong:**

  - Networking is a required part of deploying Azure Databricks.

**E. Enable anonymous public network access ❌**

- **Why it's wrong:**

  - Anonymous public access is a major security risk and is not recommended.

**Key Concept**

Best practice is to **use a custom Virtual Network and disable public IP addresses** for clusters whenever possible.

**Question 9**

**Which portal is used to centrally manage Databricks workspaces after deployment?**

**A. Azure Active Directory Portal ❌**

- **Why it's wrong:**

  - Microsoft Entra ID manages identities, not Databricks accounts and workspaces.

**B. Azure Storage Explorer ❌**

- **Why it's wrong:**

  - Storage Explorer manages Azure Storage accounts, not Databricks workspaces.

**C. account.azuredatabricks.net (Databricks Account Console) ✅ Correct**

- **Why it's correct:**

  - The Databricks Account Console is used to centrally manage:

    - Workspaces

    - Users

    - Groups

    - Identity federation

    - Unity Catalog

    - Account-level settings

**D. Azure DevOps Portal ❌**

- **Why it's wrong:**

  - Azure DevOps manages source control and CI/CD pipelines, not Databricks accounts.

**E. Microsoft Fabric Portal ❌**

- **Why it's wrong:**

  - Microsoft Fabric is a separate analytics platform and does not manage Azure Databricks workspaces.

**Key Concept**

The **Databricks Account Console** is the central management portal for account-level administration across workspaces.

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
