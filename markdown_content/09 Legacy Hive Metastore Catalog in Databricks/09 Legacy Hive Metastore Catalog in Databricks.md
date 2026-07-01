# 09 Legacy Hive Metastore Catalog in Databricks

**Legacy Hive Metastore Catalog in Databricks**

This lesson explains how Databricks managed data **before Unity Catalog** using the **Hive Metastore**. It demonstrates creating schemas, managed tables, external tables, and views, while highlighting the differences between managed and external tables.

**Key Topics Covered**

**1. Hive Metastore Before Unity Catalog**

Before Unity Catalog, Databricks used a single default catalog called the **Hive Metastore**.

Characteristics include:

- One default catalog

- Stores structured data

- Workspace-level metadata management

- No centralized governance across multiple workspaces

All tables were created under the Hive Metastore unless another catalog was available.

------------------------------------------------------------------------

**2. Starting Compute**

To work with Hive Metastore objects, a compute cluster must be running.

The lesson starts an existing compute cluster and attaches a notebook before executing SQL commands.

------------------------------------------------------------------------

**3. Default Schema**

Within the Hive Metastore, Databricks provides a default schema named:

default

If no schema is specified when creating a table, Databricks places the table into this default schema.

The lesson creates a new schema named:

CREATE SCHEMA branch;

This schema is then used to organize database objects.

------------------------------------------------------------------------

**4. Managed Tables**

The lesson creates a **Managed Table** named EMP.

Managed tables have two important characteristics:

- Databricks manages the table metadata.

- Databricks also manages the physical data files.

The table definition specifies only the schema and columns—no storage location is provided.

------------------------------------------------------------------------

**5. Two-Level Namespace**

Hive Metastore uses a **two-level namespace**:

schema.table

Example:

branch.emp

Unlike Unity Catalog, there is no catalog name because Hive Metastore contains only a single default catalog.

------------------------------------------------------------------------

**6. Table Metadata**

Using:

DESCRIBE EXTENDED branch.emp;

the lesson displays:

- Table type

- Storage location

- Storage provider

- Metadata information

This command helps users understand where Databricks stores table data.

------------------------------------------------------------------------

**7. Default Storage Location**

Managed tables are stored automatically in the Databricks-managed storage location.

Characteristics include:

- Stored in **DBFS (Databricks File System)**

- Managed by Databricks

- Located within the managed Azure resource group

- Default table format is **Delta Lake**

Users do not specify the storage path for managed tables.

------------------------------------------------------------------------

**8. Inserting and Querying Data**

The lesson inserts sample employee records into the managed table and retrieves them using:

SELECT \* FROM branch.emp;

This verifies that the table has been created successfully.

------------------------------------------------------------------------

**9. Viewing Physical Files**

Using:

dbutils.fs.ls(...)

the lesson lists the physical files stored in DBFS.

The directory contains the underlying Delta/Parquet files that make up the managed table.

------------------------------------------------------------------------

**10. External Tables**

The lesson then creates an **External Table**.

Unlike a managed table, an external table explicitly specifies a storage location using:

LOCATION '/path/...'

Characteristics:

- Metadata is stored in the metastore.

- Data remains in the user-defined storage location.

- Databricks does not own the physical data.

------------------------------------------------------------------------

**11. Comparing Managed vs External Tables**

The lesson demonstrates the most important difference.

**Managed Table**

When executing:

DROP TABLE branch.emp;

Both:

- Table metadata

- Physical data files

are deleted automatically.

------------------------------------------------------------------------

**External Table**

When executing:

DROP TABLE branch.emp_ext;

Only:

- Table metadata

is removed.

The physical data files remain in storage.

This allows the table to be recreated later using the same storage location.

------------------------------------------------------------------------

**12. Recreating an External Table**

Because the data still exists after dropping the external table, the lesson recreates the table using the same LOCATION.

Immediately after recreation:

- Metadata is restored.

- Existing data becomes accessible again.

This illustrates one of the major advantages of external tables.

------------------------------------------------------------------------

**13. Creating Views**

The lesson also creates a **View**.

A view stores a SQL query rather than data.

Example:

CREATE VIEW branch.emp_view AS\
SELECT \*\
FROM branch.emp_ext\
WHERE dept_code = 'D101';

The view filters employee records without duplicating the underlying data.

------------------------------------------------------------------------

**14. Querying Views**

Users can query the view exactly like a table:

SELECT \*\
FROM branch.emp_view;

Databricks executes the stored SQL query behind the scenes.

------------------------------------------------------------------------

**15. View Metadata**

Using:

<span class="mark">DESCRIBE EXTENDED branch.emp_view;</span>

the lesson displays:

- View definition

- Stored SQL query

- View type

- Metadata

The instructor notes that this is a **permanent view**, meaning it persists even after restarting the compute cluster.

------------------------------------------------------------------------

**Managed vs External Tables**

| **Feature**                     | **Managed Table** | **External Table** |
|---------------------------------|-------------------|--------------------|
| Metadata stored in Metastore    | ✔                 | ✔                  |
| Data managed by Databricks      | ✔                 | ✘                  |
| User specifies storage location | ✘                 | ✔                  |
| Dropping table deletes data     | ✔                 | ✘                  |
| Dropping table deletes metadata | ✔                 | ✔                  |
| Data can be reattached later    | ✘                 | ✔                  |

------------------------------------------------------------------------

**Hive Metastore vs Unity Catalog**

| **Hive Metastore** | **Unity Catalog** |
|----|----|
| Single default catalog | Multiple catalogs |
| Two-level namespace (schema.table) | Three-level namespace (catalog.schema.table) |
| Workspace-level governance | Centralized governance |
| Limited security model | Fine-grained access control |
| Legacy metadata management | Unified governance across workspaces |

------------------------------------------------------------------------

**Key Takeaways**

- Before Unity Catalog, Databricks used the **Hive Metastore** as its default catalog for structured data.

- Hive Metastore organizes objects using a **two-level namespace** (schema.table).

- **Managed tables** store both metadata and data under Databricks-managed storage; dropping the table deletes both.

- **External tables** store metadata in the metastore but keep data in a user-defined storage location; dropping the table removes only the metadata.

- **Delta Lake** is the default table format for managed tables.

- **Views** store SQL queries rather than data and provide reusable, filtered representations of underlying tables.

- Understanding the differences between managed tables, external tables, and views is essential before transitioning to the more advanced governance model provided by **Unity Catalog**.

# [README](./../../../README.md)
