# ANSWER 39 8

**Question 8**

**How does a Databricks recipient access shared data after it has been shared?**

**A. By copying all shared tables into a local metastore ❌ Incorrect**

No copying occurs.

**B. By creating a Delta Sharing Catalog that references the provider's shared objects ✅ Correct**

Workflow:

Provider

│

Share

│

Recipient

│

Creates Sharing Catalog

│

Queries Data

The catalog acts as a pointer to the provider's live data.

**C. By exporting the data to CSV files first ❌ Incorrect**

CSV export is unnecessary.

**D. By manually recreating the provider's schemas ❌ Incorrect**

The shared catalog exposes the provider's shared structure.

**E. By downloading a backup of the shared database ❌ Incorrect**

No backups are downloaded.

**Why B is correct**

Recipients create a Delta Sharing Catalog that references the provider's shared objects without copying the data.

# [README](./../../../README.md)
