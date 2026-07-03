# ANSWER 10 3

**Question 3**

**Why is an Azure Storage Account created during Unity Catalog setup?**

**A. To store Spark executors** ❌ Incorrect

- Spark executors are compute processes running on clusters.

- They are not stored in a storage account.

**B. To host Databricks notebooks** ❌ Incorrect

- Notebooks are stored within the Databricks workspace.

- The storage account is intended for managed data storage.

**C. To provide managed storage for Unity Catalog tables** ✅ Correct

Unity Catalog needs a location for managed tables.

The storage account stores:

- Delta tables

- Managed table files

- Other managed data assets

Typically this is:

Azure Storage Account\
↓\
ADLS Gen2\
↓\
Managed Storage

**D. To replace Azure Virtual Networks** ❌ Incorrect

- VNets provide networking.

- Storage Accounts provide storage.

**E. To store cluster logs only** ❌ Incorrect

- Cluster logs are only one possible use.

- Unity Catalog primarily needs the storage account for managed data.

**Key Concept**

Storage Account = Where managed table data is stored.

# [README](./../../../README.md)
