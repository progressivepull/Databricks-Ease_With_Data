# ANSWER 20 1

**Question 1**

**What is the primary purpose of a Databricks Compute (Cluster)?**

**A. To store Unity Catalog metadata** ❌ Incorrect

- Unity Catalog metadata (catalogs, schemas, permissions, lineage, etc.) is stored in the **Databricks Control Plane**.

- Clusters **use** metadata but do not store it.

**B. To execute notebooks, SQL queries, and workflows** ✅ Correct

A Databricks Compute (Cluster) is the **engine** that performs computation.

It executes:

- Notebooks

- Spark jobs

- SQL queries

- Machine Learning workloads

- Streaming jobs

- Databricks Workflows

Think of a cluster as the **computer** that performs the work.

Notebook\
\
↓\
\
Cluster\
\
↓\
\
Reads Data\
\
↓\
\
Processes Data\
\
↓\
\
Writes Results

**C. To manage Azure subscriptions** ❌ Incorrect

- Azure subscriptions are managed through the Azure Portal.

- Clusters have no role in Azure subscription management.

**D. To replace Delta Lake storage** ❌ Incorrect

- Delta Lake is the storage layer.

- Clusters process data stored in Delta Lake.

**E. To create Virtual Networks** ❌ Incorrect

- VNets are Azure networking resources.

**Memory Trick**

Cluster

↓

**Compute**

Not Storage

# [README](./../../../README.md)
