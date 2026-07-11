# ANSWER 40 10

**Question 10**

**What happens when a Serverless Compute session becomes idle?**

**A. The compute continues running indefinitely.** ❌ Incorrect

- That would waste money.

**B. The workload is automatically migrated to Classic Compute.** ❌ Incorrect

- No migration occurs.

**C. Serverless automatically terminates the idle compute session to help reduce costs.** ✅ Correct

- Databricks detects inactivity.

- Idle compute is shut down automatically.

- Resources are released.

- Costs are reduced.

**D. The notebook is deleted automatically.** ❌ Incorrect

- Only compute stops.

- The notebook remains intact.

**E. The Spark cluster is converted into a Job Cluster.** ❌ Incorrect

- Serverless does not convert clusters.

**Key Concept**

One of the biggest cost-saving features of Serverless Compute is **automatic termination of idle sessions**.

**Overall Concepts to Remember**

| **Concept** | **Remember** |
|----|----|
| Primary Goal | Eliminate cluster management |
| Managed By | Databricks |
| User Responsibility | Choose Serverless and run workloads |
| Startup Time | Seconds (pre-provisioned compute) |
| Scaling | Automatic |
| Idle Compute | Automatically terminated |
| Billing | Serverless DBUs only (infrastructure included) |
| Supported Workloads | Notebooks, Jobs, DLT, ML, SQL Warehouses |
| Supported Notebook Languages (lesson) | Python and SQL |
| Budget Policy | Cost tracking, tagging, reporting, chargeback |

# [README](./../../../README.md)
