# EXPLANATION 20 5

**Question 4**

**What is the primary advantage of Job Compute over All-Purpose Compute?**

**Correct Answer: C. It is automatically created when a workflow starts and terminated when it finishes.**

**Explanation**

Job Compute is optimized for scheduled or automated jobs.

Workflow:

Workflow Starts\
│\
Create Job Compute\
│\
Run Notebook\
│\
Complete Job\
│\
Terminate Compute

Benefits:

- No idle compute costs.

- Fresh environment for every run.

- Better resource isolation.

- Lower cloud costs.

- Ideal for production ETL pipelines.

This automatic lifecycle makes Job Compute more cost-effective than keeping an interactive cluster running all day.

**YouTube**

- **Databricks Job Compute Tutorial**\
  https://www.youtube.com/results?search_query=Databricks+Job+Compute

# [README](./../../../README.md)
