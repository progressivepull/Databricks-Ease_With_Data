# ANSWER 39 10

**Question 10**

**Which Unity Catalog feature centrally manages Delta Sharing governance?**

**A. Spark SQL Engine ❌ Incorrect**

Spark SQL executes queries.

It does not manage sharing governance.

**B. Delta Lake Transaction Log ❌ Incorrect**

The transaction log tracks table changes.

It does not manage sharing permissions.

**C. Unity Catalog manages Providers, Recipients, Shares, permissions, and security ✅ Correct**

Unity Catalog centrally manages:

- Providers

- Shares

- Recipients

- Permissions

- Authentication

- Security

- Governance

Everything related to Delta Sharing administration is managed through Unity Catalog.

Example:

Unity Catalog

│

├── Provider

├── Share

├── Recipient

├── Permissions

└── Security

**D. Databricks Connect ❌ Incorrect**

Databricks Connect allows local development against remote clusters.

It has nothing to do with Delta Sharing governance.

**E. MLflow Tracking Server ❌ Incorrect**

MLflow manages machine learning experiments and models.

It is unrelated to Delta Sharing.

**Why C is correct**

Unity Catalog is the **central governance layer** for Delta Sharing. It manages the complete sharing lifecycle—from defining **Providers** and **Recipients** to creating **Shares**, granting permissions, and enforcing security policies. This centralized governance ensures that organizations can securely share live data across teams, business units, and even external organizations while maintaining consistent access control and auditability.

# [README](./../../../README.md)
