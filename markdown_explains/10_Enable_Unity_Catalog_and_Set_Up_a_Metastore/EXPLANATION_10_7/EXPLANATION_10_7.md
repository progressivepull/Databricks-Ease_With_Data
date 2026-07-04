# EXPLANATION 10 7

**Question 7**

**Which two pieces of information are required when configuring the Metastore storage location?**

**Correct Answer:**\
✅ **ADLS Gen2 storage path and Access Connector Resource ID**

**Explanation**

When configuring managed storage for a Metastore, you provide:

**1. Storage Path**

Example:

abfss://unitycatalog@storageaccount.dfs.core.windows.net/

This tells Unity Catalog **where** to store managed data.

**2. Access Connector Resource ID**

Example:

/subscriptions/...

This identifies **which Managed Identity** should be used to authenticate to the storage account.

Together they define:

- **Where** the data lives.

- **How** Databricks securely accesses it.

**YouTube**

**Unity Catalog Storage Configuration**

https://www.youtube.com/results?search_query=Unity+Catalog+Storage+Configuration

# [README](./../../../README.md)
