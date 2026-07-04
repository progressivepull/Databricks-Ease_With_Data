# EXPLANATION 06 4

**Question 4**

**What must happen before code in a Databricks notebook can be executed?**

**Correct Answer:**\
✅ **The notebook must be attached to a Compute cluster.**

**Explanation**

A notebook contains code, but **it cannot execute code by itself**.

It must connect to a compute resource, such as:

- All-Purpose Compute

- Job Compute

- Serverless Compute (when available)

The cluster provides:

- CPU

- Memory

- Spark Driver

- Spark Executors

Workflow:

Notebook\
\
↓\
\
Attach Compute\
\
↓\
\
Run Code\
\
↓\
\
Results

Without compute, the notebook is just a document containing code.

**YouTube**

**Databricks Compute Explained**

https://www.youtube.com/results?search_query=Databricks+Compute+Explained

------------------------------------------------------------------------

# [README](./../../../README.md)
