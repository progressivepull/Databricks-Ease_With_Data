# 10 Enable Unity Catalog and Setup Metastore

**Enable Unity Catalog and Set Up a Metastore**

This lesson demonstrates how to enable **Unity Catalog** for an Azure Databricks workspace by creating a **Metastore**, provisioning Azure storage, configuring an **Access Connector**, and assigning the metastore to the workspace.

**Key Topics Covered**

**1. Why a Metastore Is Required**

Before Unity Catalog can be enabled, a **Metastore** must be created.

The Metastore is the **top-level object** in the Unity Catalog hierarchy and is responsible for managing:

- Metadata

- Permissions

- Access control

- Governance information

Without a metastore, Unity Catalog cannot function.

**2. Existing Workspace Before Unity Catalog**

Before enabling Unity Catalog:

- The workspace contains only the **Hive Metastore**.

- No additional catalogs exist.

- Users cannot create catalogs because no metastore has been assigned.

The lesson shows that the **Create Catalog** option is unavailable until a metastore is configured.

**3. Creating a Metastore**

From the Databricks **Account Console**, the instructor creates a new metastore by specifying:

- A descriptive metastore name

- Azure region

**Best Practice:**

Create **one metastore per cloud region**.

This simplifies governance and aligns with Databricks recommendations.

**4. Configure a Storage Account**

Because managed Unity Catalog tables require cloud storage, an Azure Storage Account is created.

Configuration includes:

- Existing resource group

- Unique storage account name

- Standard performance

- Locally Redundant Storage (LRS)

- Hierarchical Namespace enabled (ADLS Gen2)

Enabling the **Hierarchical Namespace** transforms Azure Blob Storage into **Azure Data Lake Storage Gen2 (ADLS Gen2)**.

**5. Create a Blob Container**

Inside the storage account, the lesson creates:

- Blob Container:

root

Inside the container, a directory named:

metastore

This directory becomes the default storage location for Unity Catalog managed tables.

**6. Create an Azure Databricks Access Connector**

Databricks requires permission to access Azure storage.

To accomplish this, an **Access Connector for Azure Databricks** is created.

The Access Connector acts as a **Managed Identity** that securely authenticates Databricks to Azure Storage without using storage keys.

**7. Assign Storage Permissions**

The Access Connector is granted the Azure role:

**Storage Blob Data Contributor**

This role allows Databricks to:

- Read data

- Write data

- Manage files

- Access the metastore storage location

The role is assigned using Azure Role-Based Access Control (RBAC).

**8. Configure the Metastore Storage Location**

Back in the Databricks Account Console, the metastore configuration requires:

- ADLS Gen2 storage path

- Access Connector Resource ID

The storage path points to:

- Storage Account

- Blob Container

- Metastore directory

This becomes the default managed storage location for Unity Catalog.

**9. Create the Metastore**

After providing:

- Region

- Storage location

- Access Connector Resource ID

the metastore is successfully created.

The Account Console confirms the metastore configuration.

**10. Assign the Metastore to a Workspace**

Creating the metastore alone does **not** enable Unity Catalog.

The metastore must also be assigned to one or more Databricks workspaces.

During assignment:

- Select the desired workspace.

- Confirm enabling Unity Catalog.

Once assigned, the workspace begins using Unity Catalog.

**11. Metastore Administrator**

The user who creates the metastore automatically becomes the **Metastore Administrator**.

Metastore Administrators can:

- Create catalogs

- Manage governance

- Configure permissions

- Administer Unity Catalog objects

This role has broader governance privileges than a Workspace Administrator.

**12. Workspace Changes After Enabling Unity Catalog**

After refreshing the workspace, several changes become visible.

New features include:

- Sample catalogs

- **Add Catalog** button

- Unity Catalog interface

- Catalog management capabilities

These features were unavailable before assigning the metastore.

**13. Catalog Creation**

Once Unity Catalog is enabled, authorized users can create catalogs directly from the workspace.

Catalog creation is available only to users with sufficient privileges, such as the Metastore Administrator.

**14. Workspace Permissions**

Returning to the Account Console shows another important change.

The **Permissions** tab becomes available for the workspace.

Administrators can now assign access to:

- Users

- Groups

- Service Principals

This enables centralized permission management through Unity Catalog.

**Overall Workflow**

1.  Verify the workspace is still using the Hive Metastore.

2.  Create a new Metastore in the Account Console.

3.  Create an Azure Storage Account.

4.  Enable ADLS Gen2.

5.  Create a Blob Container and Metastore directory.

6.  Create an Azure Databricks Access Connector.

7.  Assign the **Storage Blob Data Contributor** role.

8.  Configure the metastore storage path and Resource ID.

9.  Create the Metastore.

10. Assign the Metastore to the Databricks workspace.

11. Enable Unity Catalog.

12. Refresh the workspace.

13. Begin creating catalogs and managing permissions.

**Key Takeaways**

- A **Metastore** is the first and most important component required to enable Unity Catalog.

- Databricks recommends creating **one metastore per cloud region**.

- Managed Unity Catalog tables require an **ADLS Gen2** storage location.

- An **Azure Databricks Access Connector** (Managed Identity) securely connects Databricks to Azure Storage.

- The Access Connector must be granted the **Storage Blob Data Contributor** role to access the storage account.

- After the metastore is assigned, the workspace transitions from the **Hive Metastore** to **Unity Catalog**.

- The **Metastore Administrator** can create catalogs and manage centralized governance.

- Enabling Unity Catalog activates new capabilities, including **catalog creation**, **workspace permissions**, and centralized governance for users, groups, and Service Principals.

# [README](./../../../README.md)
