# ANSWER 22 5

**Question 5**

**What is a major advantage of using a Job Compute Cluster?**

**A. It permanently stays online after the workflow finishes.** ❌ Incorrect

- That describes All-Purpose Compute.

**B. It automatically creates Unity Catalog objects.** ❌ Incorrect

- Compute doesn't create catalogs.

**C. It is automatically created when the workflow starts and terminated when it completes or fails.** ✅ Correct

Workflow starts:

Create Cluster\
\
↓\
\
Run Tasks\
\
↓\
\
Delete Cluster

Benefits:

- Lower costs

- Fresh environment

- No idle compute

**D. It eliminates the need for Delta tables.** ❌ Incorrect

- Compute and storage are unrelated.

**E. It supports only SQL workloads.** ❌ Incorrect

- Supports notebooks, Python, SQL, Scala, and more.

------------------------------------------------------------------------

**Memory Trick**

Job Compute

↓

Temporary Cluster

------------------------------------------------------------------------

# [README](./../../../README.md)
