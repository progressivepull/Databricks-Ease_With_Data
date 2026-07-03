# ANSWER 06 4

**Question 4**

**What must happen before code in a Databricks notebook can be executed?**

**A. Unity Catalog must be enabled.** ❌ Incorrect

- Unity Catalog is optional for notebook execution.

- Notebooks can run without it.

**B. The notebook must be exported to Git.** ❌ Incorrect

- Git integration is optional.

- It is not required to run code.

**C. The notebook must be attached to a Compute cluster.** ✅ **Correct**

- Every notebook must connect to compute before executing code.

- The compute cluster provides:

  - CPUs

  - Memory

  - Spark executors

  - Spark driver

Without compute, the notebook is simply text.

**D. A Delta table must be created first.** ❌ Incorrect

- You can execute Python, SQL, or Scala without using Delta tables.

**E. A Service Principal must be configured.** ❌ Incorrect

- Service Principals are used for automation.

- Interactive notebook execution does not require one.

**Key Concept**

**Notebook = Code**\
**Compute = Engine**

Without compute, nothing runs.

------------------------------------------------------------------------

# [README](./../../../README.md)
