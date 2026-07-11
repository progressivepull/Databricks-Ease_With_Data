# ANSWER 43 1

**Question 1**

**What is the primary purpose of Lakehouse Federation in Databricks?**

**A. To automatically copy external databases into Delta Lake** ❌ Incorrect

- This describes a traditional **ETL/ELT** approach, where data is copied into the Lakehouse.

- Lakehouse Federation is specifically designed to **avoid copying data**.

- Instead, it leaves the data in the external system.

**B. To query external data sources directly without moving the data into the Lakehouse** ✅ Correct

- This is the primary purpose of Lakehouse Federation.

- It enables Databricks to query data stored in external databases through a live connection.

- The data remains in its original location.

Example:

Traditional ETL

PostgreSQL

│

Copy Data

▼

Delta Lake

│

Query

Lakehouse Federation

PostgreSQL

▲

│ Live Query

│

Databricks SQL

**C. To convert relational databases into Unity Catalog metastores** ❌ Incorrect

- Unity Catalog is a governance layer.

- External databases are **not converted** into metastores.

**D. To replace SQL Warehouses with Spark clusters** ❌ Incorrect

- SQL Warehouses are commonly used with Lakehouse Federation.

- Federation complements SQL Warehouses rather than replacing them.

**E. To automatically back up external databases into cloud storage** ❌ Incorrect

- Federation is **not** a backup solution.

- It only provides access to external data.

**Key Concept**

**Lakehouse Federation = Query external data where it already lives (no data movement).**

# [README](./../../../README.md)
