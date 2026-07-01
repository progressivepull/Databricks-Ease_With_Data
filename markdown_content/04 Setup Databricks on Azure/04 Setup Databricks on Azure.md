# 04 Setup Databricks on Azure

**Summary: Setting Up Azure Databricks on Azure**

This lesson walks through the complete process of creating an **Azure Databricks workspace** from scratch. It explains the prerequisites, pricing considerations, Azure networking setup, and deployment of a Databricks workspace integrated with Azure.

**Key Topics Covered**

**1. Databricks Cloud Platforms**

- Databricks is available on:

  - **Amazon Web Services (AWS)**

  - **Microsoft Azure**

  - **Google Cloud Platform (GCP)**

- Each cloud provider has a slightly different deployment process, so Databricks provides separate documentation for each.

**2. Pricing Considerations**

There are two types of costs when using Azure Databricks:

- **Databricks Units (DBUs)**

  - Charged based on usage of Databricks services.

  - You only pay while services are running.

- **Azure Cloud Resources**

  - Azure bills for infrastructure such as:

    - Virtual Machines

    - Storage

    - Networking

  - For example, running a cluster incurs Azure VM charges.

**3. Prerequisites**

Before creating Azure Databricks, you need:

- An Azure account

- A **Pay-As-You-Go** Azure subscription

  - Free trial subscriptions are not supported.

- A user with at least **Contributor** permissions on the subscription.

**4. Azure Databricks Integration**

- Azure Databricks is a **first-party Azure service**.

- It integrates closely with Azure services such as networking, storage, and identity.

- Because of this integration, Azure Databricks is one of Microsoft's most popular analytics services.

**5. Workspace Tiers**

Azure Databricks offers:

- **Standard**

- **Premium**

The instructor recommends using the **14-day Premium trial** because it includes additional enterprise features not available in the Standard tier.

**6. Create an Azure Resource Group**

The first Azure resource created is a **Resource Group**, which serves as a container for all related Azure resources.

The lesson also recommends adding **tags** (such as Owner) to simplify cost tracking and management.

**7. Create a Virtual Network (VNet)**

A Virtual Network is created before deploying Databricks.

Configuration includes:

- Custom private IP address space

- Reduced CIDR block (/24)

- Two subnets:

  - **Public Subnet**

  - **Private Subnet**

Each subnet receives half of the available IP addresses.

**8. Purpose of Two Subnets**

Azure Databricks requires:

- **Public subnet**

  - Handles public-facing communication.

- **Private subnet**

  - Hosts resources that should not be directly exposed to the Internet.

This improves network isolation and security.

**9. Deploy Azure Databricks Workspace**

When creating the workspace, configure:

- Subscription

- Resource Group

- Workspace Name

- Region

- Premium Trial Tier

- Managed Resource Group

- Existing Virtual Network

- Public Subnet

- Private Subnet

Networking settings connect Databricks to the previously created VNet.

**10. Networking Configuration**

During deployment:

- Disable public IP addresses.

- Select the custom Virtual Network.

- Specify:

  - Public subnet name and CIDR

  - Private subnet name and CIDR

Other settings (encryption and security) are left at their default values.

**11. Workspace Deployment**

After validation:

- Azure deploys the Databricks workspace.

- Deployment may take several minutes.

- Once complete, users can launch the workspace directly from the Azure Portal.

**12. Azure Databricks Account Console**

After deployment, users can also access:

**account.azuredatabricks.net**

The Account Console allows administrators to:

- View workspaces

- Manage workspace settings

- View pricing tier

- Configure future services such as Unity Catalog.

------------------------------------------------------------------------

**Overall Workflow**

1.  Verify Azure prerequisites.

2.  Understand Databricks and Azure pricing.

3.  Create an Azure Resource Group.

4.  Create a Virtual Network (VNet).

5.  Create Public and Private Subnets.

6.  Deploy an Azure Databricks workspace.

7.  Configure networking using the VNet.

8.  Launch the Databricks workspace.

9.  Access the Databricks Account Console for centralized management.

------------------------------------------------------------------------

**Key Takeaways**

- Azure Databricks is tightly integrated with Microsoft Azure.

- A **Pay-As-You-Go Azure subscription** and **Contributor permissions** are required.

- Costs include both **Databricks DBUs** and **Azure infrastructure charges**.

- Creating a **Virtual Network with separate public and private subnets** is an important networking best practice.

- The **Premium Trial** provides access to enterprise features for evaluation.

- After deployment, administrators manage workspaces through both the **Azure Portal** and the **Databricks Account Console**.

# [README](./../../../README.md)
