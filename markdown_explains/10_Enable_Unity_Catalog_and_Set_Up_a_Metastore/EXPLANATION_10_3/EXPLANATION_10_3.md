# EXPLANATION 10 3

**Question 3**

**Why is an Azure Storage Account created during Unity Catalog setup?**

**Correct Answer:**\
✅ **To provide managed storage for Unity Catalog tables**

**Explanation**

Unity Catalog needs a location to store **managed table data**.

In Azure, this is typically an **Azure Storage Account** with **ADLS Gen2** enabled.

The Storage Account stores:

- Delta files

- Managed table data

- Managed volume data

- Other Unity Catalog managed objects

Architecture:

Unity Catalog\
\
↓\
\
Managed Storage\
\
↓\
\
Azure Storage Account\
\
↓\
\
ADLS Gen2

The metadata is stored in the Databricks Control Plane, while the actual data resides in the customer's storage account.

**YouTube**

**Unity Catalog Managed Storage**

https://www.youtube.com/results?search_query=Unity+Catalog+Managed+Storage

# [README](./../../../README.md)
