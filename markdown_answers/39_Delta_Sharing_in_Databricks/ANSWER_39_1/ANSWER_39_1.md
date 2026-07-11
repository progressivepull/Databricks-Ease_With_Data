# ANSWER 39 1

**Question 1**

**What is the primary purpose of Delta Sharing in Databricks?**

**A. To copy Delta tables between workspaces for backup ❌ Incorrect**

- Delta Sharing is **not** a backup solution.

- It does **not** create duplicate copies of the data.

- Backup solutions involve copying or replicating data, whereas Delta Sharing allows secure access to the original data.

**B. To securely share live, read-only data across organizations, clouds, and platforms without duplicating the data ✅ Correct**

This is exactly what Delta Sharing was designed for.

It allows:

- Secure sharing

- Live access to current data

- Read-only access

- Cross-organization sharing

- Cross-cloud sharing

- Cross-platform sharing

Example:

Company A (Provider)

│

▼

Delta Sharing

│

▼

Company B (Recipient)

Company B always queries the provider's latest data.

No copies are created.

**C. To automatically synchronize Spark clusters across regions ❌ Incorrect**

- Delta Sharing shares **data**, not compute resources.

- Spark clusters remain independent.

**D. To migrate Unity Catalog metadata between metastores ❌ Incorrect**

- Metadata migration is unrelated.

- Delta Sharing shares data objects.

**E. To replace Delta Lake with Parquet files ❌ Incorrect**

- Delta Sharing actually uses Delta Lake.

- It doesn't replace it.

**Why B is correct**

Delta Sharing provides secure, live, read-only access to data without creating duplicate datasets.

# [README](./../../../README.md)
