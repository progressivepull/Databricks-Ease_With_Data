# ANSWER 08 1

**Question 1**

**What is the primary purpose of Unity Catalog in Databricks?**

**A. To optimize Spark cluster performance** ❌ Incorrect

- Spark cluster performance is improved through technologies such as **Photon**, cluster sizing, autoscaling, caching, partitioning, and query optimization.

- Unity Catalog is **not a performance optimization tool**.

- Think of Spark clusters as the **engine**, while Unity Catalog is the **security office**.

**B. To replace Delta Lake storage** ❌ Incorrect

- Delta Lake is the storage format that adds ACID transactions, Time Travel, schema enforcement, and other features.

- Unity Catalog **works with Delta Lake** but does **not replace it**.

- Delta Lake stores data; Unity Catalog manages access to the data.

**C. To provide centralized governance, security, and metadata management across Databricks workspaces** ✅ Correct\
This is exactly what Unity Catalog was built for.

It provides:

- Centralized permissions

- Fine-grained access control

- Metadata management

- Data lineage

- Auditing

- Governance across multiple workspaces

Think of Unity Catalog as the **master librarian** of your organization's data.

**D. To create Azure Virtual Networks automatically** ❌ Incorrect

- Azure Virtual Networks (VNets) are Azure infrastructure.

- They are created and managed through Azure networking.

- Unity Catalog has nothing to do with networking.

**E. To manage only SQL Warehouses** ❌ Incorrect

- Unity Catalog governs much more than SQL Warehouses.

- It governs:

  - Notebooks

  - Clusters

  - SQL Warehouses

  - ML workloads

  - APIs

  - Jobs

- Any workload accessing Unity Catalog follows the same permissions.

**Key idea:**

**Unity Catalog = Centralized Governance + Security + Metadata**

------------------------------------------------------------------------

# [README](./../../../README.md)
