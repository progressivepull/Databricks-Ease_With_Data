# ANSWER 49 2

**Question 2**

**The Databricks CLI is built on top of which underlying technology?**

**A. Apache Spark SQL Engine** ❌ Incorrect

- Spark executes distributed computations.

- It is not the communication layer used by the CLI.

**B. Databricks REST API** ✅ Correct

- Every CLI command ultimately sends requests to the Databricks REST API.

For example:

databricks catalogs list

Internally becomes:

CLI

│

REST API Request

│

Databricks

The CLI is essentially a **friendly wrapper** around the REST API.

**C. Delta Live Tables (DLT)** ❌ Incorrect

- DLT builds data pipelines.

**D. Unity Catalog Metadata Service** ❌ Incorrect

- Unity Catalog stores metadata.

- It is not the API layer.

**E. Azure Resource Manager (ARM) Templates** ❌ Incorrect

- ARM manages Azure resources, not Databricks CLI commands.

**Key Concept**

**CLI = Easier way to use the REST API.**

# [README](./../../../README.md)
