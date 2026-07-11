# ANSWER 43 10

**Question 10**

**Which pair of SQL statements can be used to automate the setup of Lakehouse Federation?**

**A. CREATE TABLE and CREATE VIEW** ❌ Incorrect

- These create database objects, not federation resources.

**B. CREATE STREAMING TABLE and REFRESH TABLE** ❌ Incorrect

- These relate to Streaming Tables, not Federation.

**C. CREATE CONNECTION and CREATE FOREIGN CATALOG** ✅ Correct

- These are the two foundational SQL statements:

1.  CREATE CONNECTION

    - Defines how to connect to the external database.

2.  CREATE FOREIGN CATALOG

    - Exposes the external database within Unity Catalog.

Workflow:

CREATE CONNECTION

│

▼

CREATE FOREIGN CATALOG

│

▼

SELECT \*

FROM foreign_catalog.schema.table;

**D. CREATE PIPELINE and CREATE JOB** ❌ Incorrect

- Pipelines and Jobs automate processing, not federation setup.

**E. CREATE DATABASE and CREATE SCHEMA** ❌ Incorrect

- These create Databricks-native objects.

**Key Concept**

**Automating Federation = CREATE CONNECTION + CREATE FOREIGN CATALOG.**

**Final Exam Summary**

| **Topic** | **Remember** |
|----|----|
| **Lakehouse Federation** | Query external data directly without copying it into the Lakehouse. |
| **Main Benefit** | Reduces storage duplication by leaving data where it already resides. |
| **Foreign Catalog** | Unity Catalog object representing an external database accessed through a live connection. |
| **First Step** | Create a **Connection** before creating a Foreign Catalog. |
| **Supported Source Example** | PostgreSQL (along with several other supported relational databases). |
| **Supported Compute** | SQL Warehouses and Classic Databricks Compute can query federated data. |
| **Foreign Tables** | Tables in a Foreign Catalog are identified as **Type = Foreign**. |
| **SQL Experience** | Use the same ANSI SQL syntax as native Unity Catalog tables; Databricks reads the data from the external database. |
| **Credential Security** | Store credentials in **Databricks Secret Scopes** or **Azure Key Vault-backed Secret Scopes**, not in SQL scripts. |
| **Federation Setup** | Use CREATE CONNECTION followed by CREATE FOREIGN CATALOG to configure access. |

# [README](./../../../README.md)
