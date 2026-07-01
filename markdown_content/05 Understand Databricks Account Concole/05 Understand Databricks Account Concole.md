# 05 Understand Databricks Account Concole

**Understanding the Databricks Account Console**

This lesson provides an overview of the **Databricks Account Console**, the centralized administrative interface used to manage Databricks accounts, workspaces, users, security, and organization-wide settings. While individual workspaces are used for development and data processing, the Account Console is where administrators manage the entire Databricks environment.

**Key Topics Covered**

**1. Purpose of the Account Console**

The Databricks Account Console is the central location for managing all Databricks workspaces within an organization. Instead of configuring each workspace individually, administrators can perform account-level administration from a single interface.

------------------------------------------------------------------------

**2. Workspace Management**

The **Workspaces** section displays every Databricks workspace associated with the account.

From here administrators can:

- View workspace information

- Configure workspace settings

- Manage security and compliance settings

- Configure workspace permissions after Unity Catalog is enabled

Each workspace can be managed independently while still being controlled from the same account.

------------------------------------------------------------------------

**3. Security and Compliance**

Each workspace contains security and compliance settings that allow administrators to configure security policies for that specific workspace.

These settings help organizations meet internal security requirements and regulatory compliance standards.

------------------------------------------------------------------------

**4. Unity Catalog Permissions**

Once **Unity Catalog** is enabled, an additional **Permissions** tab becomes available.

Administrators can grant access to:

- Individual users

- User groups

- Service Principals

This controls who can access and manage a specific Databricks workspace.

------------------------------------------------------------------------

**5. Catalogs and Metastore**

The **Catalog** section is where administrators create and manage **Metastores**.

A **Metastore** is the top-level container for Unity Catalog and stores:

- Metadata

- Permissions

- Governance information

Creating a metastore is the first step required before enabling Unity Catalog.

------------------------------------------------------------------------

**6. User Management**

The **User Management** section allows Account Administrators to manage users across the Databricks account.

Administrators can:

- View synchronized users from Microsoft Entra ID (Azure Active Directory)

- Assign or remove Account Admin privileges

- Assign Marketplace Admin privileges

- Manage account-level access

Only **Account Administrators** have permission to manage users through the Account Console.

------------------------------------------------------------------------

**7. Service Principals**

The Account Console also manages **Service Principals**.

A Service Principal is a **non-human identity** used for automation, including:

- Scheduled jobs

- Production pipelines

- CI/CD processes

- Automated workflows

Using Service Principals is considered a best practice because automated jobs should not depend on personal user accounts that may later be disabled or removed.

------------------------------------------------------------------------

**8. Groups**

Groups simplify permission management by allowing administrators to assign permissions to collections of users rather than individuals.

Typical examples include:

- HR

- Data Engineers

- Analysts

- Developers

Instead of assigning permissions user-by-user:

1.  Create a group.

2.  Grant permissions to the group.

3.  Add users or Service Principals to the group.

All members automatically inherit the group's permissions, making administration much easier in large organizations.

------------------------------------------------------------------------

**9. Network Connectivity Configurations (NCC)**

The **Network Connectivity Configurations (NCC)** section is used to securely connect Azure resources that cannot communicate directly with Databricks.

These secure networking configurations help protect communication between Databricks and cloud resources.

------------------------------------------------------------------------

**10. Preview Features**

The **Previews** section allows administrators to:

- Enable preview features

- Disable preview features

- Test new Databricks capabilities before they become generally available

This allows organizations to evaluate new functionality safely.

------------------------------------------------------------------------

**11. Account Settings**

The **Settings** section contains account-wide configuration options.

One example discussed is enabling **Serverless Compute** for:

- Workflows

- Notebooks

- Delta Live Tables (DLT)

Enabling this feature at the account level makes it available across all workspaces.

------------------------------------------------------------------------

**Why the Account Console Matters**

The Account Console provides centralized management for the entire Databricks environment. Instead of configuring dozens of workspaces separately, administrators can manage users, permissions, networking, security, and account-wide features from one location.

This becomes especially valuable for large organizations with many Databricks workspaces, where centralized administration improves consistency, simplifies governance, and reduces administrative effort.

**Key Takeaways**

- The **Account Console** is the centralized administration portal for Databricks.

- Administrators can manage **multiple workspaces** from a single location.

- **Unity Catalog permissions** are managed after creating a **Metastore**.

- **Account Administrators** control users and administrative roles.

- **Service Principals** provide secure, non-human identities for automation.

- **Groups** simplify permission management by assigning privileges collectively rather than individually.

- **Network Connectivity Configurations (NCC)** enable secure communication with Azure resources.

- The **Settings** section allows administrators to enable account-wide features such as **Serverless Compute**.

- Centralized management becomes increasingly important as organizations scale to many Databricks workspaces.

# [README](./../../../README.md)
