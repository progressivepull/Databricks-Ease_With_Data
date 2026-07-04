# EXPLANATION 06 10

**Question 10**

**Why is it recommended to terminate a compute cluster after finishing your work?**

**Correct Answer:**\
✅ **To stop Azure Virtual Machines and reduce unnecessary cloud costs**

**Explanation**

While a cluster is running:

- Azure Virtual Machines are running.

- CPU and memory are allocated.

- Billing continues even if no code is executing.

Stopping the cluster:

Running Cluster\
\
↓\
\
Terminate\
\
↓\
\
VMs Stop\
\
↓\
\
Billing Stops (for compute resources)

This is why organizations encourage developers to terminate clusters when they are no longer needed, or configure Auto Termination to do it automatically.

**YouTube**

**Databricks Cluster Management**

https://www.youtube.com/results?search_query=Databricks+Cluster+Management

------------------------------------------------------------------------

**Recommended YouTube Playlists**

If you're studying Databricks Workspaces and Notebooks, these playlists cover nearly all of these topics:

1.  **Official Databricks Training & Tutorials**

    - https://www.youtube.com/@Databricks/videos

2.  **Azure Databricks Full Course**

    - https://www.youtube.com/results?search_query=Azure+Databricks+Full+Course

3.  **Databricks Notebook Tutorial**

    - https://www.youtube.com/results?search_query=Databricks+Notebook+Tutorial

4.  **Apache Spark for Beginners**

    - https://www.youtube.com/results?search_query=Apache+Spark+for+Beginners

5.  **Databricks Workspace & Compute Tutorials**

    - https://www.youtube.com/results?search_query=Databricks+Workspace+Compute+Tutorial

# [README](./../../../README.md)
