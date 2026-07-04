# EXPLANATION 22 2

**Question 1**

**What is the primary purpose of Databricks Workflows?**

**Correct Answer: B. To orchestrate, schedule, and automate multi-step data pipelines**

**Explanation**

Databricks Workflows allows you to automate business processes instead of manually running notebooks.

A workflow can:

- Schedule jobs.

- Run multiple tasks in sequence.

- Execute tasks in parallel.

- Retry failed tasks.

- Send notifications.

- Monitor execution history.

Example ETL workflow:

Start\
│\
▼\
Load Raw Data\
│\
▼\
Clean Data\
│\
▼\
Transform Data\
│\
▼\
Write Delta Tables\
│\
▼\
Generate Reports

Instead of manually running five notebooks every day, Workflows executes them automatically.

**Why use Workflows?**

- Automation

- Repeatability

- Reliability

- Monitoring

- Scheduling

- Dependency management

**YouTube**

- **Databricks Workflows Tutorial**\
  https://www.youtube.com/results?search_query=Databricks+Workflows+Tutorial

- **Databricks Jobs and Workflows**\
  https://www.youtube.com/results?search_query=Databricks+Jobs+Workflows

------------------------------------------------------------------------

# [README](./../../../README.md)
