# EXPLANATION 03 9

**Metastore Administrator**

A **Metastore Administrator** is a user or role responsible for managing the **metadata repository (metastore)** used by a data platform. The metastore stores information **about data**, not the data itself.

**What is a Metastore?**

A **metastore** is a centralized catalog that stores metadata such as:

- Table names

- Database names

- Column names and data types

- Table locations (such as cloud storage paths)

- Partitions

- Views

- Permissions

- Data ownership

- Tags and descriptions

For example, instead of searching cloud storage for a file, a metastore knows:

Database: sales\
Table: customers\
Location: s3://company-data/sales/customers/\
Columns:\
customer_id INT\
name STRING\
state STRING

**Responsibilities of a Metastore Administrator**

A Metastore Administrator typically has the highest level of permissions over the metastore.

**1. Create and Manage Catalogs**

Creates logical collections of databases.

Example:

Catalog\
├── Sales\
├── Finance\
└── Marketing

**2. Create Databases (Schemas)**

Example SQL:

CREATE SCHEMA sales;

**3. Register Tables**

The administrator can register existing cloud storage data as tables.

Example:

CREATE TABLE sales.orders\
USING DELTA\
LOCATION 's3://company/orders';

**4. Manage Permissions**

Grant or revoke access to users and groups.

Example:

GRANT SELECT\
ON TABLE sales.orders\
TO analysts;

or

REVOKE INSERT\
ON TABLE sales.orders\
FROM interns;

**5. Configure External Storage**

Connect cloud storage locations.

Examples include:

- Amazon S3

- Azure Data Lake Storage

- Google Cloud Storage

**6. Manage External Locations**

Define which storage paths users may access.

Example:

External Location:\
\
Name:\
finance_data\
\
Path:\
s3://company-finance/

**7. Set Up Storage Credentials**

Configure secure authentication for cloud storage using mechanisms such as:

- IAM roles

- Service principals

- Managed identities

**8. Manage Data Sharing**

In platforms that support data sharing, administrators can control which catalogs, schemas, or tables are shared with other organizations or workspaces.

**9. Audit Metadata**

Monitor:

- Who created tables

- Who deleted tables

- Permission changes

- Metadata updates

- Access history

**10. Configure Governance Policies**

Set organization-wide policies for:

- Naming conventions

- Data classifications

- Tags

- Retention

- Security rules

**Typical Permissions**

A Metastore Administrator can typically:

| **Action**                | **Allowed** |
|---------------------------|-------------|
| Create catalogs           | ✅          |
| Delete catalogs           | ✅          |
| Create schemas            | ✅          |
| Grant permissions         | ✅          |
| Manage users/groups       | ✅          |
| Register storage          | ✅          |
| Create external locations | ✅          |
| Audit activity            | ✅          |
| Configure governance      | ✅          |

**Example in Databricks**

In platforms like Databricks, a Metastore Administrator manages the **Unity Catalog metastore** for an organization.

Typical responsibilities include:

- Creating catalogs

- Assigning catalog owners

- Configuring storage credentials

- Creating external locations

- Managing data access

- Enabling secure data sharing

- Monitoring metadata and audit logs

**Why the Role Matters**

Without a Metastore Administrator:

- Teams may not know what datasets exist.

- Duplicate or inconsistent tables can proliferate.

- Permissions may become overly broad or insecure.

- Data governance becomes difficult.

- Auditing and compliance are harder to enforce.

A Metastore Administrator helps ensure that data assets are **organized, secure, discoverable, and governed**, enabling analysts, data engineers, and data scientists to work efficiently while maintaining proper access controls.

Here are some high-quality YouTube videos that explain **Metastore Administrator**, **Unity Catalog**, and related Databricks administration topics.

**1. Setting up Databricks Unity Catalog Environments**

- **Advancing Spark - Setting up Databricks Unity Catalog Environments**

> [**https://www.youtube.com/watch?v=B0Ox7jdoPNQ**](https://www.youtube.com/watch?v=B0Ox7jdoPNQ)

This video covers:

- Creating a metastore

- Assigning workspaces

- Configuring catalogs

- Understanding the responsibilities of a Metastore Administrator

**2. Enable Unity Catalog and Set Up a Metastore**

- **10 Enable Unity Catalog and Setup Metastore \| How to setup Unity Catalog for Databricks Workspace**

> [**https://www.youtube.com/watch?v=NHQcq-ubOig**](https://www.youtube.com/watch?v=NHQcq-ubOig)

Topics include:

- Creating a Unity Catalog metastore

- Configuring storage

- Assigning a metastore to a workspace

- Initial administration tasks

> **Official Documentation**
>
> **For a detailed explanation of the Metastore Administrator role:**

- **[Databricks – Admin privileges in Unity Catalog](https://docs.databricks.com/gcp/en/data-governance/unity-catalog/manage-privileges/admin-privileges?utm_source=chatgpt.com)**

- **[Microsoft Learn – Unity Catalog Setup Guide](https://learn.microsoft.com/en-us/azure/databricks/data-governance/unity-catalog/setup-uc?utm_source=chatgpt.com)**

> These resources explain the differences between:

- Account Admin

- Workspace Admin

- Metastore Admin

> and the permissions associated with each role.
>
> <https://docs.databricks.com/gcp/en/data-governance/unity-catalog/manage-privileges/admin-privileges?utm_source=chatgpt.com>

# [README](./../../../README.md)
