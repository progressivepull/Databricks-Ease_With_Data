# ANSWER 20 10

**Question 10**

**Which cluster permission allows a user to attach notebooks and execute code, but not start, stop, edit, or delete the cluster?**

**A. Can Manage** ❌ Incorrect

- Highest permission level.

- Allows editing, deleting, and managing the cluster.

**B. Can Restart** ❌ Incorrect

- Allows starting and stopping the cluster.

- More privileges than needed.

**C. Can Attach To** ✅ Correct

This permission allows users to:

✅ Attach notebooks

✅ Execute code

But **cannot**:

❌ Edit cluster configuration

❌ Delete cluster

❌ Change permissions

❌ Manage settings

This is commonly granted to notebook developers.

**D. Cluster Owner** ❌ Incorrect

- Full administrative control.

**E. Workspace Administrator** ❌ Incorrect

- Workspace Administrator is a workspace-wide role, not a cluster permission.

**Memory Trick**

Need to use the cluster?

↓

**Can Attach To**

Need to manage the cluster?

↓

**Can Manage**

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| Databricks Compute (Cluster) | Executes notebooks, SQL queries, Spark jobs, ML workloads, and workflows |
| Driver Node | Coordinates the cluster, runs the Spark Driver, schedules tasks, and collects results |
| Best compute for development | **All-Purpose Compute** |
| Main advantage of Job Compute | Automatically created for a job and automatically terminated when the job finishes |
| Unity Catalog multi-user access mode | **Shared** |
| Recommended Databricks Runtime | **Latest Long-Term Support (LTS)** release |
| Photon | High-performance execution engine that accelerates SQL, ETL, streaming, and data science workloads |
| Auto Scaling | Automatically increases or decreases the number of worker nodes based on workload demand |
| Auto Termination | Stops idle clusters after a configured time to reduce cloud costs |
| Cluster permission for running notebooks | **Can Attach To** (run code without managing the cluster) |

# [README](./../../../README.md)
