# EXPLANATION 03 8

**Databricks Account Administrator Explained**

Using the office-building analogy:

| **Real World** | **Databricks**        |
|----------------|-----------------------|
| Building Owner | Account Administrator |
| Building       | Databricks Account    |
| Office Suite   | Workspace             |
| Employees      | Users                 |
| Computers      | Clusters              |

An **Account Administrator** is the highest-level administrator in a Databricks account. They manage the entire Databricks environment across all workspaces.

**What an Account Administrator Can Do**

**1. Create and Manage Workspaces**

- Create new workspaces

- Delete workspaces

- Configure workspace settings

Example:

- Create separate workspaces for Development, Test, and Production.

**2. Manage Users and Groups**

- Add users

- Remove users

- Create groups

- Assign roles

Example:

- Add a new data engineer to the "Data Engineering" group.

**3. Assign Admin Roles**

- Grant Workspace Admin privileges

- Grant additional Account Admin privileges

**4. Manage Identity and Authentication**

- Configure SSO (Single Sign-On)

- Configure SCIM provisioning

- Manage identity federation

**5. Manage Security and Governance**

- Configure Unity Catalog at the account level

- Manage metastores

- Set account-wide policies

**6. Monitor Account Usage**

- View billing information

- Review usage reports

- Manage cloud integrations

------------------------------------------------------------------------

**Account Admin vs Workspace Admin**

| **Responsibility**        | **Account Admin** | **Workspace Admin** |
|---------------------------|-------------------|---------------------|
| Create Workspace          | ✅                | ❌                  |
| Delete Workspace          | ✅                | ❌                  |
| Manage All Users          | ✅                | Limited             |
| Manage Account Settings   | ✅                | ❌                  |
| Manage Workspace Settings | ✅                | ✅                  |
| Create Clusters           | Usually ✅        | ✅                  |
| Manage Unity Catalog      | ✅                | Limited             |

**Example Scenario**

Suppose a company has:

Databricks Account\
├── Dev Workspace\
├── Test Workspace\
└── Prod Workspace

**Account Administrator**

- Creates all three workspaces

- Adds employees

- Configures security

- Sets up Unity Catalog

**Workspace Administrator**

- Manages users and resources within a specific workspace (for example, only the Dev workspace)

**Interview Answer**

An Account Administrator is the highest-level administrator in Databricks. They manage the Databricks account, including workspaces, users, groups, authentication, billing, and governance settings such as Unity Catalog. Account Admins have visibility and control across all workspaces in the account.

------------------------------------------------------------------------

Here are some of the best YouTube videos for learning the **Databricks Account Administrator** role:

**1. Administrator Best Practices and Tips for Future-Proofing Your Databricks Account**

🔗 <https://www.youtube.com/watch?v=QPTi-aFH7fs>

Covers:

- Account administration

- User onboarding

- Security best practices

- Workspace management at scale

------------------------------------------------------------------------

**2. Databricks Architecture Explained: Accounts, Workspaces, and Key Roles**

🔗 <https://www.youtube.com/watch?v=bTybxljtdho>

Covers:

- Account Admin

- Workspace Admin

- Metastore Admin

- Control Plane vs Data Plane

- Databricks architecture

------------------------------------------------------------------------

**3. Databricks Admin Roles 101**

🔗 <https://www.youtube.com/watch?v=fkbCKDtz2SE>

Covers:

- Account Admin responsibilities

- Workspace Admin responsibilities

- Access management

- Governance roles

------------------------------------------------------------------------

**4. Understand Databricks Account Console \| User Management \| Workspace Management**

🔗 <https://www.youtube.com/watch?v=tMOORviaZ14>

Covers:

- Account Console

- User management

- Service principals

- Workspace administration

- Metastore creation

------------------------------------------------------------------------

**5. User Management in Databricks \| Users, Service Principals & Groups**

🔗 <https://www.youtube.com/watch?v=rtqvQG7AZFc>

Covers:

- Adding users

- Groups

- SCIM provisioning

- Identity management

- Unity Catalog administration

------------------------------------------------------------------------

**Quick Interview Answer**

**Account Administrator** is the highest-level administrator in Databricks. They manage:

- Accounts

- Workspaces

- Users and groups

- Identity federation

- Unity Catalog

- Security and governance

- Billing and usage

**Memory Trick:**\
🏢 **Account Admin = Building Owner**\
🚪 **Workspace Admin = Office Manager**\
👨‍💼 **Users = Employees**\
💻 **Clusters = Computers**\
📄 **Notebooks = Documents**

# [README](./../../../README.md)
