# 11 Catalog, External Location & Storage Credentials in Unity Catalog

**Catalogs, External Locations, and Storage Credentials in Unity Catalog**

This lesson explains how to create **Catalogs** in Unity Catalog and introduces **Storage Credentials** and **External Locations**, which allow managed tables to store their data in user-defined cloud storage instead of the default metastore location.

**Key Topics Covered**

**1. Managed Storage Hierarchy in Unity Catalog**

Unity Catalog stores managed table data according to a **fallback hierarchy**.

The hierarchy is:

Metastore\
↓\
Catalog\
↓\
Schema\
↓\
Managed Table

When a managed table is created, Databricks determines where to store the data using the following priority:

1.  **Schema Managed Location** (highest priority)

2.  **Catalog Managed Location**

3.  **Metastore Managed Location** (default)

If no managed location is defined at the schema or catalog level, the table's data is stored in the metastore location.

------------------------------------------------------------------------

**2. Why Managed Locations Matter**

Managed locations allow organizations to control where managed table data is physically stored.

For example:

- Finance catalog → Finance storage account

- HR catalog → HR storage account

- Development catalog → Development storage account

This provides better organization, governance, and storage isolation.

**3. Metastore Managed Location**

The lesson reviews the metastore created previously.

Its managed location becomes the default storage location for all managed tables unless a lower-level managed location overrides it.

Databricks automatically appends a unique metastore identifier to the configured storage path.

------------------------------------------------------------------------

**4. Creating Storage for Catalogs**

To demonstrate catalog-level storage, the lesson creates additional Azure Storage folders.

Inside the existing storage account:

- Blob Container

data

Inside that container:

ADB/

Then:

Catalog/

This directory becomes the root storage location for catalog-managed data.

------------------------------------------------------------------------

**5. Creating the First Catalog**

Using the Catalog Explorer UI, the instructor creates a catalog named:

dev

Characteristics:

- Standard catalog

- No managed location specified

Because no managed location is configured, all managed tables created inside this catalog will inherit the **metastore managed location**.

------------------------------------------------------------------------

**6. Catalogs Automatically Contain Schemas**

After creation, Databricks automatically creates:

- default

- information_schema

These schemas are available immediately inside every new catalog.

------------------------------------------------------------------------

**7. Using SQL to Create Catalogs**

Catalogs can also be created with SQL.

Example:

CREATE CATALOG DevSQL\
COMMENT 'Catalog created using SQL';

SQL allows automation and scripting of Unity Catalog administration.

------------------------------------------------------------------------

**8. Legacy Clusters and Unity Catalog**

The lesson encounters an error:

Unity Catalog is not enabled on this cluster.

This occurs because the compute cluster was created **before** Unity Catalog was enabled.

To resolve this:

- Edit the cluster.

- Reconfigure it.

- Restart it.

After reconfiguration, the cluster displays the **Unity Catalog** tag and can access Unity Catalog objects.

------------------------------------------------------------------------

**9. Viewing Catalog Properties**

Using:

DESCRIBE CATALOG EXTENDED dev;

the instructor displays catalog metadata including:

- Owner

- Comments

- Storage location

- Creation details

Since no managed location was specified, no storage path appears.

------------------------------------------------------------------------

**10. Dropping Catalogs**

A catalog can be deleted using:

DROP CATALOG DevSQL;

Initially, the command fails because catalogs contain schemas.

Using:

DROP CATALOG DevSQL CASCADE;

recursively deletes:

- Tables

- Views

- Schemas

- Other objects

- Catalog

**Warning:** CASCADE permanently removes all objects within the catalog.

------------------------------------------------------------------------

**11. Storage Credentials**

Before creating an external location, Unity Catalog requires a **Storage Credential**.

A Storage Credential acts as a secure bridge between:

- Databricks

- Cloud Storage

On Azure, it uses a **Managed Identity (Access Connector)** to authenticate without storage keys.

------------------------------------------------------------------------

**12. Creating a Storage Credential**

The lesson creates a Storage Credential by:

- Selecting Azure Managed Identity

- Providing the Azure Access Connector Resource ID

- Naming the credential

The credential references the same Azure Access Connector created earlier for the metastore.

------------------------------------------------------------------------

**13. External Locations**

An **External Location** represents a registered cloud storage path that Unity Catalog can manage securely.

It consists of:

- Cloud storage URL

- Storage Credential

The lesson creates an external location using SQL:

CREATE EXTERNAL LOCATION ...

This registers the Azure Data Lake Storage path with Unity Catalog.

------------------------------------------------------------------------

**14. Creating a Catalog with a Managed Location**

A second catalog is created:

dev_ext

Unlike the first catalog, this one specifies:

- Managed Location

- External Location

As a result, managed tables created inside this catalog store their data beneath the catalog-managed storage path instead of the metastore location.

------------------------------------------------------------------------

**15. Catalog Storage Path**

Running:

<span class="mark">DESCRIBE CATALOG EXTENDED dev_ext;</span>

shows:

- Storage Root

- Catalog ID

- Managed Location

Databricks automatically appends internal Unity Catalog directories beneath the specified storage path.

------------------------------------------------------------------------

**Storage Location Fallback**

| **Managed Location Defined At** | **Where Managed Tables Are Stored** |
|---------------------------------|-------------------------------------|
| Schema                          | Schema location                     |
| Catalog                         | Catalog location                    |
| Metastore                       | Metastore location (default)        |

------------------------------------------------------------------------

**Components Introduced**

| **Component** | **Purpose** |
|----|----|
| Metastore | Stores metadata and default managed storage location |
| Catalog | Top-level data container that can define its own managed location |
| Storage Credential | Securely connects Unity Catalog to cloud storage |
| External Location | Registered cloud storage path managed by Unity Catalog |
| Managed Location | Physical storage location for managed tables |

------------------------------------------------------------------------

**Key Takeaways**

- Managed table storage follows a **fallback hierarchy**: **Schema → Catalog → Metastore**.

- If no catalog or schema managed location is defined, managed tables use the **Metastore managed location**.

- A **Catalog** can be created through the Databricks UI or SQL.

- Existing compute clusters created before enabling Unity Catalog must be updated before they can access Unity Catalog objects.

- **Storage Credentials** securely connect Unity Catalog to Azure Storage using a **Managed Identity (Access Connector)**.

- **External Locations** register cloud storage paths that Unity Catalog can govern.

- Catalogs with a configured **Managed Location** store managed tables in their own storage path rather than the metastore's default location.

- The DESCRIBE CATALOG EXTENDED command displays catalog metadata, including ownership, comments, and managed storage information.

- The DROP CATALOG ... CASCADE command removes a catalog and all of its contained objects, so it should be used with caution.

# [README](./../../../README.md)
