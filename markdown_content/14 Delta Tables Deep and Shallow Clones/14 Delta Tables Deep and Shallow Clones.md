# 14 Delta Tables Deep and Shallow Clones

**Delta Tables, Utility Commands, Views, CTAS, Deep Clone, and Shallow Clone**

This lesson explores several useful SQL and Spark utility commands for working with Unity Catalog, introduces **temporary and permanent views**, and explains three methods of copying Delta tables: **CTAS (Create Table As Select)**, **Deep Clone**, and **Shallow Clone**. It also demonstrates Delta Lake's versioning and time travel capabilities.

**Key Topics Covered**

**1. Listing Catalogs, Schemas, and Tables**

The lesson begins with several SQL utility commands for exploring Unity Catalog.

**List all catalogs**

SHOW CATALOGS;

**Filter catalogs**

SHOW CATALOGS LIKE 'dev\*';

**List schemas in a catalog**

SHOW SCHEMAS IN dev;

**List tables in a schema**

SHOW TABLES IN dev.bronze;

**Filter tables**

SHOW TABLES IN dev.bronze LIKE 'sales\*';

These commands help users quickly discover Unity Catalog objects.

**2. Checking Whether a Table Exists**

Using PySpark, the lesson demonstrates checking for a table's existence.

Example:

spark.catalog.tableExists("dev.bronze.sales_external")

Returns:

- **True** if the table exists

- **False** otherwise

This is useful when writing automation or deployment scripts.

**3. Creating Tables Safely**

The instructor creates an employee table using:

CREATE TABLE IF NOT EXISTS ...

Using **IF NOT EXISTS** prevents errors if the object already exists.

The same option can also be used when creating:

- Catalogs

- Schemas

- Tables

Without this clause, SQL raises an error if the object already exists.

**4. Delta Table History**

After inserting data into the Delta table, the lesson displays its transaction history using:

DESCRIBE HISTORY table_name;

The history includes:

- Version number

- Operation performed

- Timestamp

- User

- Operation details

Every write operation creates a new Delta version.

**5. Delta Time Travel**

Delta Lake allows querying previous versions of a table.

Example:

SELECT \*\
FROM table_name VERSION AS OF 1;

Earlier versions show the state of the table before later inserts occurred.

This provides built-in auditing and historical analysis.

**6. Temporary Views**

A temporary view is created using:

CREATE TEMP VIEW ...

Characteristics:

- Stores only a SQL query

- Does not duplicate data

- Exists only during the current compute session

- Automatically disappears when the cluster terminates

Temporary views are useful for intermediate analysis.

**7. Permanent Views**

Permanent views are created using:

CREATE VIEW ...

Characteristics:

- Stored in Unity Catalog

- Persist after cluster shutdown

- Store only the SQL definition

- Do not physically duplicate data

Views act as reusable virtual tables.

**8. Replacing Views**

Existing views can be updated using:

CREATE OR REPLACE VIEW ...

This replaces the stored SQL definition without requiring the view to be dropped first.

**Copying Delta Tables**

The lesson compares three methods of creating copies of existing tables.

**1. CTAS (Create Table As Select)**

Example:

CREATE TABLE emp_ctas\
AS\
SELECT \*\
FROM emp;

CTAS creates:

- New table

- New physical storage

- Copy of the current data

The new table is independent of the original.

However, some metadata (such as partitioning or certain table properties) may not be fully preserved.

**2. Deep Clone**

Deep Clone creates a complete duplicate of a Delta table.

Example:

CREATE TABLE emp_dc\
DEEP CLONE emp;

Deep Clone copies:

- Metadata

- Schema

- Table properties

- Partition information

- Data files

The cloned table becomes an independent Delta table with its own storage location.

The clone begins from the latest version of the source table.

**Advantages of Deep Clone**

Compared to CTAS:

- Preserves all metadata

- Copies Delta transaction history information

- Produces a true replica

- Safer for production migrations

Deep Clone is generally preferred over CTAS when duplicating Delta tables.

**3. Shallow Clone**

Shallow Clone behaves differently.

Example:

<span class="mark">CREATE TABLE emp_sc\
SHALLOW CLONE emp;</span>

Shallow Clone copies:

- Metadata

- Table definition

Initially, it **does not copy the physical data files**.

Instead, it references the data files of the original table.

This makes shallow cloning much faster and requires far less storage.

**Source Version**

A shallow clone points to the specific Delta version that existed when the clone was created.

Even if additional rows are later inserted into the original table, the shallow clone continues referencing its original version.

**Independent Changes**

If new rows are inserted directly into the shallow clone:

- Those new records are stored in the shallow clone's own storage.

- The original table is unaffected.

The clone becomes partially independent while still referencing the original data for unchanged records.

**Effect of Vacuum**

The instructor notes an important limitation.

Since shallow clones initially depend on the original table's data files, aggressive **VACUUM** operations on the source table can affect shallow clones by removing files they reference.

**Comparison of Copy Methods**

| **Feature**              | **CTAS** | **Deep Clone** | **Shallow Clone** |
|--------------------------|----------|----------------|-------------------|
| Copies metadata          | Partial  | ✔              | ✔                 |
| Copies physical data     | ✔        | ✔              | ✘ (initially)     |
| Independent storage      | ✔        | ✔              | Partial           |
| Preserves Delta metadata | Limited  | ✔              | ✔                 |
| Fast creation            | Moderate | Moderate       | Very Fast         |
| Minimal storage usage    | ✘        | ✘              | ✔                 |
| References original data | ✘        | ✘              | ✔                 |

**Views Comparison**

| **Feature**                  | **Temporary View** | **Permanent View** |
|------------------------------|--------------------|--------------------|
| Stores data                  | ✘                  | ✘                  |
| Stores SQL query             | ✔                  | ✔                  |
| Exists after cluster restart | ✘                  | ✔                  |
| Stored in Unity Catalog      | ✘                  | ✔                  |

**Key Takeaways**

- Unity Catalog provides SQL commands such as **SHOW CATALOGS**, **SHOW SCHEMAS**, and **SHOW TABLES** to explore metadata.

- PySpark's spark.catalog.tableExists() method allows applications to verify whether a table exists before performing operations.

- Delta Lake automatically tracks every table modification, enabling **transaction history** and **time travel** through DESCRIBE HISTORY and versioned queries.

- **Temporary Views** exist only for the current compute session, while **Permanent Views** persist in Unity Catalog and store reusable SQL definitions without duplicating data.

- **CTAS (Create Table As Select)** creates a new table with copied data but may not preserve all Delta metadata.

- **Deep Clone** creates a complete, independent copy of a Delta table, including its metadata and data, making it ideal for backups, migrations, and production copies.

- **Shallow Clone** copies only metadata and initially references the original table's data files, providing fast, storage-efficient cloning while remaining isolated from future source table changes unless affected by operations such as **VACUUM**.

# [README](./../../../README.md)
