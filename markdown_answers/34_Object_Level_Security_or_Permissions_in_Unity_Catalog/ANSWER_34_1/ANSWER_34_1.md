# ANSWER 34 1

**Question 1**

**What is the primary purpose of Object-Level Security in Unity Catalog?**

**A. To automatically optimize Delta tables for performance ❌ Incorrect**

- Table optimization is handled by features like:

  - OPTIMIZE

  - Z-Ordering

  - Predictive Optimization

  - Photon

- Object-Level Security controls **permissions**, not performance.

**B. To encrypt all data stored in Unity Catalog ❌ Incorrect**

- Encryption is handled by the cloud storage platform (Azure Storage, Amazon S3, Google Cloud Storage).

- Unity Catalog manages **authorization and governance**, not storage encryption.

**C. To control who can view, access, modify, and manage individual Unity Catalog objects ✅ Correct**

Object-Level Security allows administrators to control access to objects such as:

- Catalogs

- Schemas

- Tables

- Views

- Volumes

- Functions

- Models

Example:

Sales Catalog

↓

Sales Schema

↓

Orders Table

Permissions can determine:

- Who can see the catalog

- Who can query the table

- Who can modify data

- Who can change permissions

**D. To create catalogs and schemas automatically ❌ Incorrect**

- Unity Catalog can store these objects.

- It does not automatically create them.

**E. To manage Spark cluster configurations ❌ Incorrect**

- Cluster configuration is handled by Databricks Compute.

- Object-Level Security is unrelated to Spark clusters.

**Why C is correct**

Object-Level Security provides **fine-grained access control** over Unity Catalog objects, ensuring users have only the permissions they need.

# [README](./../../../README.md)
