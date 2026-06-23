# ANSWER 03 9

**Which role is responsible for creating catalogs and managing data objects?**

A. Workspace Administrator\
**B. Metastore Administrator**\
C. Account Administrator\
D. Owner\
E. Service Principal

**Correct Answer: B**

**First Understand the Hierarchy**

A common exam trick is to test whether you know the scope of each role.

Think of Databricks administration as four levels:

| **Level** | **Role** | **Focus** |
|----|----|----|
| Account | Account Administrator | Entire Databricks account |
| Metastore | Metastore Administrator | Unity Catalog governance |
| Workspace | Workspace Administrator | One workspace |
| Object | Owner | Specific object (table, schema, notebook, etc.) |

------------------------------------------------------------------------

**Option A: Workspace Administrator ❌ Wrong**

A Workspace Administrator manages a specific workspace.

Responsibilities:

- Manage workspace users

- Manage workspace permissions

- Manage notebooks

- Manage workspace assets

Example:

- Add Alice to Workspace A

- Remove Bob from Workspace B

- Manage notebook permissions inside a workspace

**Why Wrong?**

The question asks about:

Creating catalogs and managing data objects

Catalogs belong to **Unity Catalog governance**, which is managed at the **metastore level**, not the workspace level.

Think:

**Workspace Admin = Workspace Management**

NOT

**Workspace Admin = Data Governance**

------------------------------------------------------------------------

**Option B: Metastore Administrator ✅ Correct**

The Metastore Administrator is responsible for Unity Catalog governance.

Responsibilities:

- Create catalogs

- Manage schemas

- Manage tables

- Manage data objects

- Delegate privileges

- Govern data access

Example:

Metastore\
│\
├── Catalog: Sales\
│ ├── Schema: Finance\
│ └── Table: Revenue\
│\
├── Catalog: Marketing\
│\
└── Catalog: HR

The Metastore Administrator can create and manage these structures.

**Why Correct?**

The question specifically asks:

Creating catalogs and managing data objects

Those are core Metastore Administrator responsibilities.

This is almost a direct definition from the Databricks role descriptions.

------------------------------------------------------------------------

**Option C: Account Administrator ❌ Wrong**

The Account Administrator manages the Databricks account itself.

Responsibilities:

- Create workspaces

- Manage users

- Manage groups

- Manage service principals

- Manage metastores

- Assign metastores to workspaces

Example:

Account\
│\
├── Workspace Dev\
├── Workspace UAT\
├── Workspace Prod\
│\
├── Users\
├── Groups\
└── Metastore

**Why Wrong?**

The Account Administrator manages the metastore itself but does **not typically create catalogs and schemas inside the metastore**.

Think of it like:

- Account Admin = Creates the building

- Metastore Admin = Organizes the rooms inside the building

The exam often tries to confuse these two roles.

------------------------------------------------------------------------

**Option D: Owner ❌ Wrong**

An Owner is the creator of a specific object.

Examples:

- Table owner

- Schema owner

- Notebook owner

Responsibilities:

- Manage that object

- Grant permissions on that object

Example:

Sarah creates:

Sales.CRM.Customers

Sarah becomes the owner of that table.

She can:

- Grant SELECT access

- Transfer ownership

- Manage permissions

**Why Wrong?**

Owners manage objects they own.

They do not have broad responsibility for:

- Creating catalogs across the organization

- Managing Unity Catalog governance

That responsibility belongs to the Metastore Administrator.

------------------------------------------------------------------------

**Option E: Service Principal ❌ Wrong**

A Service Principal is not an administrator role.

It is a non-human identity used by:

- Applications

- Automation scripts

- CI/CD pipelines

- Scheduled jobs

Example:

GitHub Actions\
↓\
Service Principal\
↓\
Databricks Workspace

The Service Principal authenticates and accesses resources securely.

**Why Wrong?**

A Service Principal is an identity, not a governance role.

It does not create catalogs or manage data governance.

------------------------------------------------------------------------

**Quick Elimination Strategy for the Exam**

When you see:

**Account-wide tasks**

Think:\
➡️ **Account Administrator**

Examples:

- Workspaces

- Users

- Groups

- Service Principals

- Metastores

------------------------------------------------------------------------

**Unity Catalog tasks**

Think:\
➡️ **Metastore Administrator**

Examples:

- Catalogs

- Schemas

- Tables

- Data governance

- Privilege delegation

------------------------------------------------------------------------

**Workspace tasks**

Think:\
➡️ **Workspace Administrator**

Examples:

- Workspace users

- Workspace permissions

- Workspace assets

------------------------------------------------------------------------

**Object-level tasks**

Think:\
➡️ **Owner**

Examples:

- Table ownership

- Notebook ownership

- Schema ownership

------------------------------------------------------------------------

**Automation identity**

Think:\
➡️ **Service Principal**

Examples:

- CI/CD

- Automated jobs

- Applications

------------------------------------------------------------------------

**Memory Trick**

**"Catalogs live in a Metastore."**

So if the question mentions:

- Catalogs

- Schemas

- Data governance

- Unity Catalog

The answer is almost always:

✅ **Metastore Administrator**.

# [README](./../../../README.md)
