# ANSWER 20 4

**Question 4**

**What is the primary advantage of Job Compute over All-Purpose Compute?**

**A. It supports only SQL workloads.** ❌ Incorrect

- Job Compute supports Spark, Python, SQL, Scala, and more.

**B. It remains running permanently after the job completes.** ❌ Incorrect

- That's the opposite of Job Compute.

**C. It is automatically created when a workflow starts and terminated when it finishes.** ✅ Correct

Workflow:

Job Starts\
\
↓\
\
Create Cluster\
\
↓\
\
Run Notebook\
\
↓\
\
Cluster Terminates

Benefits:

- Lower cloud costs

- Fresh environment

- No idle compute charges

**D. It requires manual startup before every scheduled job.** ❌ Incorrect

- Job Compute is automated.

**E. It does not support Unity Catalog.** ❌ Incorrect

- Job Compute fully supports Unity Catalog.

**Memory Trick**

Job Compute

↓

Temporary Cluster

# [README](./../../../README.md)
