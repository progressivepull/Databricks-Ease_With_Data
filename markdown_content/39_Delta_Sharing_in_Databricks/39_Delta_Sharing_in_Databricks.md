# 39 Delta Sharing in Databricks

**Delta Sharing in Databricks**

This lesson introduces **Delta Sharing**, Databricks' open protocol for securely sharing live data across organizations, clouds, and platforms. Delta Sharing enables organizations to share **read-only** data without copying or duplicating it. The lesson covers both **Databricks-to-Databricks sharing** and **Open Sharing**, along with the configuration steps, permissions, recipients, providers, and catalogs required for sharing data.

------------------------------------------------------------------------

**1. What is Delta Sharing?**

Delta Sharing is an open protocol that allows organizations to securely share live data.

It supports sharing:

- Across organizations

- Across cloud providers

- Across Databricks workspaces

- Across metastores

- With non-Databricks platforms

Unlike exporting data, Delta Sharing provides controlled access to the source data without creating copies.

------------------------------------------------------------------------

**2. Read-Only Sharing**

Delta Sharing is **read-only**.

Recipients can:

- Query data

- Read tables

- Read volumes

- Read shared functions

Recipients **cannot**:

- Insert data

- Update data

- Delete data

- Modify shared objects

This protects the source organization's data while enabling collaboration.

------------------------------------------------------------------------

**3. Two Sharing Modes**

Delta Sharing supports two sharing methods.

**Databricks-to-Databricks Sharing**

Used when both organizations use Databricks.

Example:

Organization A\
\
↓\
\
Databricks\
\
↓\
\
Organization B\
\
↓\
\
Databricks

------------------------------------------------------------------------

**Open Sharing**

Used when the recipient does **not** use Databricks.

Supported consumers include:

- Apache Spark

- Power BI

- Python applications

- Other tools supporting the Delta Sharing protocol

Databricks\
\
↓\
\
Delta Sharing\
\
↓\
\
Spark\
\
Power BI\
\
Python

------------------------------------------------------------------------

**4. External vs Internal Sharing**

Delta Sharing supports two scenarios.

**External Organization**

Requires enabling Delta Sharing at the Metastore level.

**Internal Sharing**

Sharing between different metastores in the same organization.

Internal sharing does **not** require enabling external sharing.

------------------------------------------------------------------------

**5. Enabling Delta Sharing**

To share data with external organizations:

Enable Delta Sharing at the Metastore.

Configuration includes:

- Organization name

- Token lifetime

- External sharing enabled

Once enabled, Unity Catalog manages secure sharing tokens.

------------------------------------------------------------------------

**6. Required Permissions**

Users who create shares require several Metastore-level permissions.

Examples include:

- CREATE SHARE

- CREATE RECIPIENT

- CREATE PROVIDER

Recipients need corresponding usage permissions to access shared data.

These permissions are managed through Unity Catalog.

------------------------------------------------------------------------

**7. Delta Sharing Components**

Delta Sharing uses four main objects.

Provider\
\
↓\
\
Share\
\
↓\
\
Recipient\
\
↓\
\
Catalog

Each plays a different role in the sharing process.

------------------------------------------------------------------------

**8. Provider**

The **Provider** is the organization that shares the data.

Responsibilities:

- Owns the data

- Creates shares

- Grants recipients access

Example:

Azure Databricks\
\
↓\
\
Provider

------------------------------------------------------------------------

**9. Recipient**

The **Recipient** is the organization receiving the shared data.

A recipient may be:

- Another Databricks workspace

- Another company

- An Open Sharing client

Recipients never own the source data.

They only receive read-only access.

------------------------------------------------------------------------

**10. Share**

A **Share** is the package of objects being shared.

It may contain:

- Tables

- Views

- Volumes

- Functions

Example:

Bronze Share\
\
↓\
\
20 Tables\
\
Volumes\
\
Functions

------------------------------------------------------------------------

**11. Databricks-to-Databricks Workflow**

Overall process:

Provider\
\
↓\
\
Recipient\
\
↓\
\
Share\
\
↓\
\
Create Catalog\
\
↓\
\
Query Data

The recipient creates a catalog that references the provider's shared objects.

------------------------------------------------------------------------

**12. Creating a Recipient**

The first step is creating a recipient.

Information required:

- Recipient name

- Sharing method

- Sharing identifier

For Databricks-to-Databricks sharing, the sharing identifier is copied from the recipient workspace.

------------------------------------------------------------------------

**13. Sharing Identifier**

Each Databricks workspace exposes a unique **Sharing Identifier**.

Workflow:

Recipient Workspace\
\
↓\
\
Sharing Identifier\
\
↓\
\
Provider\
\
↓\
\
Recipient Created

This identifier securely links the provider with the recipient.

------------------------------------------------------------------------

**14. Creating a Share**

After creating the recipient:

Create a Share.

Example:

Bronze Share

The share contains selected Unity Catalog objects.

Only objects for which the provider has sufficient permissions can be shared.

------------------------------------------------------------------------

**15. Permissions Required for Shared Objects**

Because Delta Sharing is read-only, the provider must have permissions such as:

- SELECT (Tables)

- READ VOLUME (Volumes)

- EXECUTE (Functions)

These permissions allow the objects to be included in a share.

------------------------------------------------------------------------

**16. Recipient Workflow**

After data is shared:

Recipient sees:

Shared With Me

The recipient then creates a **Delta Sharing Catalog**.

Example:

Shared Catalog\
\
↓\
\
Bronze Schema\
\
↓\
\
Tables\
\
Volumes\
\
Functions

The shared objects appear like native Unity Catalog objects.

**17. Shared Objects**

The lesson demonstrates sharing:

- Bronze schema

- Tables

- Volumes

- Functions

After creating the shared catalog, the recipient can browse and query all authorized objects.

------------------------------------------------------------------------

**18. Open Sharing**

Open Sharing allows non-Databricks consumers to access shared data.

Supported technologies include:

- Apache Spark

- Python

- Power BI

- Other applications supporting the Delta Sharing protocol

Instead of using Databricks workspace authentication, Open Sharing uses sharing tokens.

------------------------------------------------------------------------

**19. Token-Based Sharing**

For Open Sharing:

Provider\
\
↓\
\
Token\
\
↓\
\
Recipient\
\
↓\
\
Delta Sharing Client

The token authenticates access to the shared data.

Token expiration can be configured when enabling Delta Sharing.

------------------------------------------------------------------------

**20. Delta Sharing Libraries**

Open Sharing clients use the official **Delta Sharing libraries**.

Examples include:

- Python SDK

- Apache Spark connector

- Other open-source clients

These libraries connect to the provider using the Delta Sharing protocol.

------------------------------------------------------------------------

**21. Unity Catalog Integration**

Delta Sharing is fully managed by Unity Catalog.

Unity Catalog controls:

- Providers

- Recipients

- Shares

- Permissions

- Governance

- Security

This ensures that sharing follows the same governance model as other Unity Catalog objects.

**22. Databricks-to-Databricks vs Open Sharing**

| **Feature** | **Databricks-to-Databricks** | **Open Sharing** |
|----|----|----|
| Recipient uses Databricks | Yes | No |
| Authentication | Workspace sharing identifier | Sharing token |
| Unity Catalog required | Yes | Provider uses Unity Catalog |
| Client | Databricks Workspace | Spark, Python, Power BI, etc. |
| Read-only | Yes | Yes |

------------------------------------------------------------------------

**23. End-to-End Architecture**

Provider Organization\
\
↓\
\
Unity Catalog\
\
↓\
\
Delta Share\
\
↓\
\
Recipient\
\
↓\
\
Shared Catalog\
\
↓\
\
Tables\
Views\
Volumes\
Functions

The provider governs access, while recipients consume the data through a shared catalog or Delta Sharing client.

------------------------------------------------------------------------

**Best Practices**

- Use **Delta Sharing** instead of copying datasets when collaborating across teams or organizations to ensure consumers always access current, governed data.

- Choose **Databricks-to-Databricks Sharing** when both parties use Unity Catalog-enabled Databricks workspaces.

- Use **Open Sharing** when recipients use tools such as Apache Spark, Python, or Power BI instead of Databricks.

- Grant only the minimum required permissions (such as **SELECT**, **READ VOLUME**, and **EXECUTE**) before adding objects to a share.

- Remember that Delta Sharing is **read-only**—recipients can query shared objects but cannot modify the provider's data.

- Manage Providers, Recipients, Shares, and permissions through **Unity Catalog** to maintain centralized governance and security

# [README](./../../../README.md)
