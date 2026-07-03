# ANSWER 10 7

**Question 7**

**Which two pieces of information are required when configuring the Metastore storage location?**

**A. Cluster ID and Workspace URL** ❌ Incorrect

- Clusters are unrelated to metastore storage.

**B. ADLS Gen2 storage path and Access Connector Resource ID** ✅ Correct

You must provide:

1.  Storage location

Example:

abfss://unitycatalog@storageaccount.dfs.core.windows.net/

2.  Access Connector Resource ID

This tells Azure which Managed Identity is allowed to access the storage.

Together they provide:

- Where the data lives

- Who is allowed to access it

**C. Subscription ID and Spark Version** ❌ Incorrect

- Neither is used when configuring managed storage.

**D. Notebook path and SQL Warehouse ID** ❌ Incorrect

- These are unrelated.

**E. Catalog name and Schema name** ❌ Incorrect

- Catalogs and schemas are created after the metastore exists.

**Key Concept**

Need:

- Storage Path

- Access Connector Resource ID

# [README](./../../../README.md)
