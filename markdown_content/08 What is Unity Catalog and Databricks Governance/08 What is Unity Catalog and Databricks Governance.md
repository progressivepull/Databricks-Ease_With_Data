# 08 What is Unity Catalog and Databricks Governance

**Unity Catalog and Governance in Databricks**

This lesson introduces **Unity Catalog**, Databricks' unified governance solution. It explains how Unity Catalog centralizes security, access control, auditing, and metadata management across multiple Databricks workspaces while simplifying data governance.

**Key Topics Covered**

**1. What is Data Governance?**

Data governance is the practice of ensuring that organizational data is:

- Secure

- Available

- Accurate

- Properly managed

Databricks addresses these requirements through **Unity Catalog**, which provides centralized governance for data and AI assets.

------------------------------------------------------------------------

**2. What is Unity Catalog?**

Unity Catalog is Databricks' **open-source unified governance solution**.

Its primary principle is:

**Define security once and enforce it everywhere.**

Instead of managing permissions separately in every workspace, Unity Catalog centralizes governance at the account level.

Unity Catalog provides:

- Centralized security

- Fine-grained access control

- Data auditing

- Data lineage

- Data discovery

- Metadata management

Being open source also allows the community to inspect and contribute to its development.

------------------------------------------------------------------------

**3. Benefits of Centralized Governance**

Without Unity Catalog:

- Each workspace manages its own users.

- Permissions are configured separately.

- Governance is decentralized.

- Administration becomes difficult as the number of workspaces grows.

With Unity Catalog:

- Governance is managed from one central location.

- Policies are applied consistently across workspaces.

- User management becomes significantly simpler.

- Security remains consistent throughout the organization.

------------------------------------------------------------------------

**4. Unity Catalog Object Model**

Unity Catalog organizes its objects in a hierarchy.

The hierarchy begins with the **Metastore**, followed by data and non-data objects.

<span class="mark">Metastore\
│\
├── Catalog\
│ ├── Schema\
│ │ ├── Tables\
│ │ ├── Views\
│ │ ├── Volumes\
│ │ ├── Functions\
│ │ └── ML Models\
│\
├── Storage Credentials\
├── External Locations\
├── Shares\
├── Recipients\
├── Providers\
├── Connections\
└── Clean Rooms</span>

Understanding this hierarchy is essential because every governed object belongs somewhere within this structure.

------------------------------------------------------------------------

**5. Metastore**

The **Metastore** is the top-level object in Unity Catalog.

Its responsibilities include storing metadata such as:

- Table definitions

- Schemas

- Permissions

- Access Control Lists (ACLs)

- Governance information

The lesson also explains the storage architecture:

- **Metadata** is stored in the **Databricks Control Plane**.

- **Actual data files** remain in the customer's **Data Plane** (cloud storage).

A best practice is to create **one metastore per cloud region**.

------------------------------------------------------------------------

**6. Catalog**

The **Catalog** is the highest-level **data securable object**.

Catalogs organize an organization's major collections of data.

Examples might include:

- Finance

- Sales

- Marketing

- Development

- Production

Permissions granted at the catalog level can cascade to lower-level objects.

------------------------------------------------------------------------

**7. Schema**

Schemas organize related database objects within a catalog.

A schema typically contains:

- Tables

- Views

- Functions

- Volumes

Schemas help logically separate data within a catalog.

------------------------------------------------------------------------

**8. Tables and Views**

Tables and Views store and present **structured data**.

Examples include:

- Transaction tables

- Customer records

- Reporting views

These objects are fully governed through Unity Catalog permissions.

------------------------------------------------------------------------

**9. Volumes**

Volumes provide managed file storage inside Unity Catalog.

They can store:

- Structured data

- Semi-structured data

- Unstructured data

Examples include:

- CSV files

- JSON files

- Images

- Documents

- Machine learning datasets

Access to files stored in Volumes is controlled through Unity Catalog.

------------------------------------------------------------------------

**10. Functions**

Unity Catalog also governs reusable SQL functions.

Functions perform reusable business logic while remaining secured through Unity Catalog permissions.

------------------------------------------------------------------------

**11. ML Models**

Machine Learning models can also be governed by Unity Catalog.

This allows organizations to manage model access using the same security framework applied to their data assets.

------------------------------------------------------------------------

**12. Non-Data Securable Objects**

Unity Catalog also manages supporting infrastructure objects, including:

- Storage Credentials

- External Locations

- Shares

- Recipients

- Providers

- Connections

- Clean Rooms

Although these objects do not directly store business data, they support secure access and data sharing.

------------------------------------------------------------------------

**13. Three-Level Namespace**

One of the biggest changes introduced by Unity Catalog is the **three-level namespace**.

Every table is referenced using:

catalog.schema.table

Example:

dev.branch.sales

Where:

- **dev** = Catalog

- **branch** = Schema

- **sales** = Table

This naming convention uniquely identifies every data object and allows permissions to be enforced consistently.

------------------------------------------------------------------------

**Why Unity Catalog Is Important**

Unity Catalog replaces workspace-specific governance with a centralized governance model.

Benefits include:

- Single source of truth for permissions

- Consistent security across workspaces

- Simplified administration

- Better auditing and compliance

- Built-in data lineage

- Easier discovery of organizational data assets

- Unified governance for both data and AI assets

**Key Takeaways**

- **Unity Catalog** is Databricks' centralized, open-source governance solution.

- It allows administrators to **define security once and enforce it across all workspaces**.

- The **Metastore** is the top-level governance object that stores metadata, permissions, and governance information.

- Metadata resides in the **Control Plane**, while actual data remains in the customer's **Data Plane**.

- **Catalogs**, **Schemas**, **Tables**, **Views**, **Volumes**, **Functions**, and **ML Models** are all governed by Unity Catalog.

- Supporting objects such as **Storage Credentials**, **External Locations**, and **Clean Rooms** help enable secure access and data sharing.

- Unity Catalog introduces the **three-level namespace** (catalog.schema.table), providing a standardized way to identify and secure every data object.

- Centralized governance simplifies security, administration, compliance, and collaboration across multiple Databricks workspaces.

# [README](./../../../README.md)
