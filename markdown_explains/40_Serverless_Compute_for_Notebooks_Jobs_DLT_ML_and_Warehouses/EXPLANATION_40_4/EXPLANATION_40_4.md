# EXPLANATION 40 4

**Question 4**

**Why do Serverless notebooks and jobs typically start within seconds?**

**Correct Answer:**

**B. Databricks maintains a fleet of pre-provisioned virtual machines ready to run workloads.**

------------------------------------------------------------------------

**Why B is Correct**

Classic clusters require:

- VM allocation

- Spark startup

- Runtime installation

This can take minutes.

Serverless keeps pre-warmed resources available, enabling startup in seconds.

------------------------------------------------------------------------

**Why the others are wrong**

It's **not** because:

- Spark is faster

- Delta is cached

- Storage changed

The improvement comes from pre-provisioned infrastructure.

------------------------------------------------------------------------

**Memory Tip**

Pre-warmed VMs = Fast startup.

------------------------------------------------------------------------

**Individual Video**

[https://www.youtube.com/watch?v=uyDykcGxELM](https://www.youtube.com/watch?v=uyDykcGxELM&utm_source=chatgpt.com)

**Search**

https://www.youtube.com/results?search_query=Databricks+Serverless+startup

------------------------------------------------------------------------

# [README](./../../../README.md)
