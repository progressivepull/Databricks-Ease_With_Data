# ANSWER 22 1

**Question 1**

**What is the primary purpose of Databricks Workflows?**

**A. To optimize Delta Lake storage only** ❌ Incorrect

- Storage optimization is handled by commands such as:

OPTIMIZE table_name;\
VACUUM table_name;

- Workflows can **call** these commands, but they are not limited to storage optimization.

**B. To orchestrate, schedule, and automate multi-step data pipelines** ✅ Correct

Databricks Workflows is the orchestration service for Databricks.

It can:

- Run notebooks

- Run Python scripts

- Execute SQL

- Run Delta Live Tables (DLT)

- Trigger JARs

- Schedule jobs

- Manage dependencies

- Retry failed tasks

- Send notifications

Think of it as the **conductor of an orchestra**—it coordinates many individual tasks into one automated pipeline.

Example:

Extract Data\
↓\
Clean Data\
↓\
Transform Data\
↓\
Load Delta Table\
↓\
Send Email

Each step is automated by a Workflow.

**C. To replace Unity Catalog** ❌ Incorrect

- Unity Catalog provides governance, security, and metadata.

- Workflows execute processes.

- They solve completely different problems.

**D. To create Spark clusters automatically for notebooks only** ❌ Incorrect

- Workflows can automatically create Job Compute clusters.

- They support many task types—not just notebooks.

**E. To manage Azure subscriptions** ❌ Incorrect

- Azure subscriptions are managed in Azure Portal.

------------------------------------------------------------------------

**Memory Trick**

Workflows =

Schedule\
\
Automate\
\
Orchestrate

------------------------------------------------------------------------

# [README](./../../../README.md)
