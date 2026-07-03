# ANSWER 23 6

**Question 6**

**Where does COPY INTO maintain metadata about previously processed files?**

**A. Azure Active Directory** ❌ Incorrect

- Azure AD manages identities.

**B. Unity Catalog Metastore only** ❌ Incorrect

- Unity Catalog stores metadata about tables and permissions.

- File ingestion history is tracked elsewhere.

**C. The Delta transaction log (\_delta_log)** ✅ Correct

Every Delta table contains:

\_delta_log

This log tracks:

- Transactions

- Loaded files

- Operations

- Versions

COPY INTO checks this log to determine which files have already been processed.

**D. Spark UI** ❌ Incorrect

- Spark UI displays execution details.

**E. DBFS root directory** ❌ Incorrect

- DBFS is not where ingestion metadata is stored.

**Memory Trick**

Delta Table

↓

\_delta_log

↓

Knows Which Files Were Loaded

# [README](./../../../README.md)
