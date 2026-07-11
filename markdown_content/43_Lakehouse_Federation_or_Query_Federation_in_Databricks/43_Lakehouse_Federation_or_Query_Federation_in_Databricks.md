# 43 Lakehouse Federation or Query Federation in Databricks

**Lakehouse Federation (Query Federation) in Databricks**

This lesson introduces **Lakehouse Federation** (also called **Query Federation**) in Databricks. Lakehouse Federation allows Databricks to query data stored in external databases **without copying or moving the data into the Lakehouse**. Databricks creates a secure connection to external systems, exposes them as **Foreign Catalogs** in Unity Catalog, and enables SQL queries, governance, permissions, and lineage on the external data.

------------------------------------------------------------------------

**1. What is Lakehouse Federation?**

Lakehouse Federation is a feature that allows Databricks to query external data sources directly.

Instead of:

External Database\
\
↓\
\
Copy Data\
\
↓\
\
Lakehouse

Databricks performs:

External Database\
\
↓\
\
Live Connection\
\
↓\
\
Databricks Query

The data remains in the source system while Databricks queries it in place.

------------------------------------------------------------------------

**2. Why Use Lakehouse Federation?**

Many organizations already store data in databases such as:

- PostgreSQL

- MySQL

- Oracle

- SQL Server

- Other supported systems

Rather than migrating all of that data into Databricks, Lakehouse Federation lets users analyze it directly.

Benefits include:

- No data migration

- Reduced storage duplication

- Faster onboarding

- Unified governance through Unity Catalog

------------------------------------------------------------------------

**3. Example Scenario**

The lesson demonstrates connecting Databricks to a PostgreSQL database.

The external database contains:

PostgreSQL\
\
↓\
\
Department Table\
\
Employee Table

Databricks queries these tables directly without importing them into Delta Lake.

------------------------------------------------------------------------

**4. Foreign Catalogs**

Lakehouse Federation introduces a new catalog type.

Unity Catalog supports:

- Standard Catalog

- Shared Catalog

- **Foreign Catalog**

A **Foreign Catalog** represents external data accessed through a live connection.

Unity Catalog\
\
↓\
\
Foreign Catalog\
\
↓\
\
External Database

------------------------------------------------------------------------

**5. Connection**

Before querying external data, a **Connection** must be created.

The connection stores information such as:

- Database type

- Hostname

- Port

- Username

- Password

Example:

Databricks\
\
↓\
\
Connection\
\
↓\
\
PostgreSQL

------------------------------------------------------------------------

**6. Supported Databases**

The lesson shows PostgreSQL, but Databricks supports many connection types.

Examples include:

- PostgreSQL

- MySQL

- Oracle

- SQL Server

- Other supported relational databases

Each connection type has its own configuration settings.

------------------------------------------------------------------------

**7. SQL Warehouse Requirement**

Testing the connection requires compute.

Supported compute includes:

- Serverless SQL Warehouse

- Pro SQL Warehouse

- Classic Databricks Compute

These environments include the drivers necessary to connect to external databases.

------------------------------------------------------------------------

**8. Creating a Foreign Catalog**

After a successful connection test:

Databricks creates:

Connection\
\
↓\
\
Foreign Catalog\
\
↓\
\
External Tables

The Foreign Catalog appears alongside standard Unity Catalog catalogs.

------------------------------------------------------------------------

**9. Foreign Tables**

Tables inside a Foreign Catalog are marked as:

Type = Foreign

These tables are **not stored in Delta Lake**.

They remain in the external database while Databricks exposes them through Unity Catalog.

------------------------------------------------------------------------

**10. Querying External Data**

After the Foreign Catalog is created, SQL queries work exactly like queries against native Unity Catalog tables.

Example workflow:

SQL Query\
\
↓\
\
Foreign Table\
\
↓\
\
PostgreSQL\
\
↓\
\
Results

Users do not need to learn a different SQL syntax.

------------------------------------------------------------------------

**11. Example Join**

The lesson joins:

- Employee

- Department

Workflow:

Employee\
\
↓\
\
JOIN\
\
↓\
\
Department\
\
↓\
\
Employee Count by Department

The query executes through Databricks while reading data from PostgreSQL.

------------------------------------------------------------------------

**12. Multiple Catalogs**

A single connection can create multiple Foreign Catalogs.

Example:

PostgreSQL Connection\
\
↓\
\
Catalog A\
\
Catalog B\
\
Catalog C

Each catalog can expose different databases or schemas from the same external system.

------------------------------------------------------------------------

**13. Unity Catalog Governance**

Foreign Catalogs remain governed by Unity Catalog.

Administrators can manage:

- Permissions

- Ownership

- Catalog access

- Schema access

- Table access

External data follows the same security model as native Databricks objects.

------------------------------------------------------------------------

**14. Lineage**

Lakehouse Federation integrates with Unity Catalog Lineage.

Benefits include:

- Track query usage

- Identify downstream consumers

- Trace data back to external sources

This provides governance even when the data remains outside the Lakehouse.

------------------------------------------------------------------------

**15. Sample Data**

Catalog Explorer allows users to preview data from Foreign Tables.

Workflow:

Foreign Table\
\
↓\
\
Sample Data\
\
↓\
\
Live Query

The preview reads directly from the external database.

------------------------------------------------------------------------

**16. SQL-Based Configuration**

The lesson demonstrates using the UI but also notes that Lakehouse Federation can be configured entirely with SQL.

Two key SQL statements are available:

**Create Connection**

CREATE CONNECTION

**Create Foreign Catalog**

CREATE FOREIGN CATALOG

This enables Infrastructure-as-Code and automated deployments.

------------------------------------------------------------------------

**17. Secrets Integration**

Instead of hardcoding database credentials, SQL connections can retrieve:

- Username

- Password

from **Databricks Secret Scopes** or **Azure Key Vault-backed Secret Scopes**.

This improves security by keeping credentials out of SQL scripts.

**18. End-to-End Architecture**

External Database\
\
↓\
\
Connection\
\
↓\
\
Foreign Catalog\
\
↓\
\
Unity Catalog\
\
↓\
\
SQL Warehouse\
\
↓\
\
SQL Query\
\
↓\
\
Results

Databricks queries the external source while applying Unity Catalog governance and metadata management.

------------------------------------------------------------------------

**19. Benefits of Lakehouse Federation**

Advantages include:

- No ETL required

- No data duplication

- Query live operational databases

- Centralized governance

- Unified security

- Lineage support

- SQL access through Databricks

This makes it easier to analyze data across systems without first loading everything into the Lakehouse.

------------------------------------------------------------------------

**Lakehouse Federation vs Data Ingestion**

| **Feature** | **Lakehouse Federation** | **Data Ingestion** |
|----|----|----|
| Data copied into Lakehouse | No | Yes |
| Queries external source directly | Yes | No |
| Storage duplication | No | Yes |
| Supports Unity Catalog governance | Yes | Yes |
| Best for | Live operational data | Analytical workloads requiring local storage |

------------------------------------------------------------------------

**Best Practices**

- Use **Lakehouse Federation** when you need to analyze external databases without copying data into the Lakehouse.

- Create **Connections** and **Foreign Catalogs** through Unity Catalog so external data is governed consistently with native Databricks objects.

- Protect database credentials by storing usernames and passwords in **Databricks Secret Scopes** or **Azure Key Vault-backed Secret Scopes** instead of embedding them in SQL.

- Run federated queries through **Serverless** or **Pro SQL Warehouses**, which include the required database drivers.

- Apply Unity Catalog permissions and use **Lineage** to maintain governance and traceability for external data sources.

- Use SQL-based creation commands (CREATE CONNECTION and CREATE FOREIGN CATALOG) when automating deployments or managing infrastructure as code.

# [README](./../../../README.md)
