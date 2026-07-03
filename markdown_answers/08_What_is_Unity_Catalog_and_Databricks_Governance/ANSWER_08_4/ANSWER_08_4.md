# ANSWER 08 4

**Question 4**

**Where is Unity Catalog metadata stored?**

**A. Customer Data Plane only** ❌ Incorrect

- Customer data lives in the Data Plane.

- Metadata does not.

**B. Azure Virtual Network** ❌ Incorrect

- Networks carry traffic.

- They do not store Unity Catalog metadata.

**C. Databricks Control Plane** ✅ Correct

Metadata includes:

- Catalogs

- Schemas

- Tables

- Permissions

- Ownership

- Lineage

- Policies

These are managed by the Databricks service in the **Control Plane**.

**D. Delta Lake transaction log only** ❌ Incorrect

- Delta logs track table changes.

- They do not store Unity Catalog governance information.

**E. Unity Catalog Volume** ❌ Incorrect

- Volumes store files.

- Metadata is stored in the Control Plane.

**Key idea**

Control Plane stores:

- Metadata

- Governance

- Security

- Configuration

Data Plane stores:

- Actual customer data

------------------------------------------------------------------------

# [README](./../../../README.md)
