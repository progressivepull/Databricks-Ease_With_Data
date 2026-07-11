# ANSWER 39 6

**Question 6**

**What information is required to create a Databricks-to-Databricks recipient?**

**A. Cluster ID and notebook path ❌ Incorrect**

Clusters and notebooks are unrelated.

**B. Workspace URL and SQL Warehouse ID ❌ Incorrect**

Not sufficient.

**C. Recipient name, sharing method, and the recipient workspace's Sharing Identifier ✅ Correct**

Typical information includes:

- recipient name

- Databricks-to-Databricks sharing

- Sharing Identifier

The Sharing Identifier uniquely identifies the recipient workspace.

**D. Delta table location and storage account key ❌ Incorrect**

Storage keys are not needed.

**E. Unity Catalog metastore ID only ❌ Incorrect**

Not enough information.

**Why C is correct**

The Sharing Identifier securely identifies the recipient workspace during Databricks-to-Databricks sharing.

# [README](./../../../README.md)
