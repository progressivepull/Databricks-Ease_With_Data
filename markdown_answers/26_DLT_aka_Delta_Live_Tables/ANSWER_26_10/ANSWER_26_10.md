# ANSWER 26 10

**Question 10**

**What information does the automatically generated DLT Directed Acyclic Graph (DAG) provide?**

**A. Only cluster CPU and memory usage ❌ Incorrect**

Those are cluster metrics, not the DLT DAG.

**B. Dataset dependencies, processing order, record counts, and execution progress ✅ Correct**

The DAG visually shows:

- how datasets depend on one another

- execution order

- pipeline progress

- record counts flowing between datasets

- successes and failures

Example:

Raw Files

│

▼

Bronze

│

▼

Silver

│

▼

Gold

This makes it much easier to understand, monitor, and troubleshoot pipeline execution.

**C. Source code history for every notebook ❌ Incorrect**

Source code history is handled by version control systems such as Git, not the DLT DAG.

**D. Cloud storage pricing information ❌ Incorrect**

The DAG has nothing to do with cloud billing or storage costs.

**E. User permissions for Unity Catalog ❌ Incorrect**

Permissions are managed through Unity Catalog and are not displayed in the DLT DAG.

**Why B is correct**

The DLT DAG is an automatically generated visualization of the entire pipeline. It helps you understand:

- **Dataset dependencies** (which datasets rely on others)

- **Processing order** (what runs first, next, and last)

- **Record counts** (how much data flows through each stage)

- **Execution progress** (current status, successes, failures, and pipeline health)

This visualization is one of DLT's most valuable features for monitoring and troubleshooting complex ETL

# [README](./../../../README.md)
