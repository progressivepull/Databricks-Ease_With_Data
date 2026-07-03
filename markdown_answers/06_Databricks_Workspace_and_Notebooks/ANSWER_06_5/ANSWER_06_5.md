# ANSWER 06 5

**Question 5**

**Which configuration is recommended to reduce cloud costs when creating a compute cluster?**

**A. Enable Photon Acceleration only** ❌ Incorrect

- Photon improves performance.

- It does not automatically reduce idle costs.

**B. Increase the number of worker nodes** ❌ Incorrect

- More workers generally increase costs.

**C. Enable Auto Termination** ✅ **Correct**

- Auto Termination automatically shuts down idle clusters after a specified period.

- This prevents paying for unused virtual machines.

Example:

- Finish work at 5 PM

- Cluster automatically shuts down after 20 minutes of inactivity

- No overnight cloud charges

**D. Disable Spark Session creation** ❌ Incorrect

- Spark Sessions are required for Spark processing.

- Disabling them would prevent workloads from running.

**E. Use only multi-node clusters** ❌ Incorrect

- Multi-node clusters typically cost more than single-node clusters.

**Key Concept**

One of the easiest ways to save money in Databricks is enabling **Auto Termination**.

------------------------------------------------------------------------

# [README](./../../../README.md)
