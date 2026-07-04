# EXPLANATION 22 6

**Question 5**

**What is a major advantage of using a Job Compute Cluster?**

**Correct Answer: C. It is automatically created when the workflow starts and terminated when it completes or fails.**

**Explanation**

Job Compute exists only while the workflow runs.

Lifecycle:

Workflow Starts\
│\
Create Compute\
│\
Run Tasks\
│\
Workflow Ends\
│\
Terminate Compute

Benefits:

- Lower cloud costs.

- Fresh environment for every run.

- Automatic cleanup.

- Better resource isolation.

- No idle clusters.

This makes Job Compute ideal for scheduled production pipelines.

**YouTube**

- **Databricks Job Compute**\
  https://www.youtube.com/results?search_query=Databricks+Job+Compute

------------------------------------------------------------------------

# [README](./../../../README.md)
