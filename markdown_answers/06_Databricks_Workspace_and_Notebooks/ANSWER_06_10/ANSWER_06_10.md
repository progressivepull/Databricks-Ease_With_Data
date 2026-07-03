# ANSWER 06 10

**Question 10**

**Why is it recommended to terminate a compute cluster after finishing your work?**

**A. To permanently delete the notebook** ❌ Incorrect

- Notebooks remain saved in the Workspace.

- Terminating a cluster does not affect notebook files.

**B. To enable Unity Catalog automatically** ❌ Incorrect

- Unity Catalog is independent of cluster termination.

**C. To stop Azure Virtual Machines and reduce unnecessary cloud costs** ✅ **Correct**

- Compute clusters run on cloud virtual machines.

- Leaving a cluster running while idle continues to incur charges.

- Terminating the cluster:

  - Stops the virtual machines

  - Stops billing for compute resources

  - Saves cloud costs

**D. To increase Spark performance for future jobs** ❌ Incorrect

- Restarting a cluster does not inherently improve Spark performance.

- Performance depends on cluster configuration and workload.

**E. To convert notebooks into SQL scripts** ❌ Incorrect

- Cluster termination has no effect on notebook formats.

**Key Concept**

A running cluster means **running cloud virtual machines**, and running virtual machines mean **ongoing costs**. Terminating idle clusters is a simple but important best practice for controlling cloud spending.

# [README](./../../../README.md)
