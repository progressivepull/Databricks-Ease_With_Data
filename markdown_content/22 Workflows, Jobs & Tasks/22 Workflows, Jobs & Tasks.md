# 22 Workflows, Jobs & Tasks

**Workflows, Jobs, and Tasks in Databricks**

This lesson introduces **Databricks Workflows**, a feature used to orchestrate, schedule, and automate data pipelines. It explains the relationship between **Jobs** and **Tasks**, demonstrates the Workflow user interface, and shows how notebooks, parameters, conditional logic, and looping can be combined to build automated ETL workflows.

------------------------------------------------------------------------

**Key Topics Covered**

**1. What are Databricks Workflows?**

Databricks **Workflows** provide orchestration capabilities for data pipelines.

A workflow allows you to:

- Schedule jobs

- Execute notebooks

- Run SQL scripts

- Trigger Python programs

- Execute Delta Live Tables (DLT)

- Coordinate multiple processing steps

Workflows automate end-to-end data processing instead of requiring manual notebook execution.

------------------------------------------------------------------------

**2. Job vs. Task**

A **Job** is a complete workflow.

A **Task** is an individual step inside the workflow.

Job\
│\
├── Task 1\
├── Task 2\
├── Task 3\
└── Task 4

A job may contain one task or dozens of dependent tasks.

------------------------------------------------------------------------

**3. Example Workflow**

The lesson builds a workflow that:

1.  Determines the current day.

2.  Checks whether today is Sunday.

3.  If today is Sunday:

    - Process employee data.

    - Split employees by department.

    - Write department-specific Delta tables.

4.  Otherwise:

    - Skip processing.

This demonstrates how business logic can control workflow execution.

------------------------------------------------------------------------

**4. Workflow User Interface**

Creating a workflow begins by selecting:

Create Job

The first step is assigning a job name.

Example:

Process Employee Data by Department

The job then becomes a container for multiple tasks.

------------------------------------------------------------------------

**Tasks**

**5. Task Types**

Databricks supports many task types.

Examples include:

- Notebook

- Python Script

- Python Wheel

- SQL

- Delta Live Tables (DLT)

- dbt

- Spark Submit

- Run Another Job

- If / Else

- For Each

This allows workflows to combine multiple technologies within a single pipeline.

------------------------------------------------------------------------

**6. Notebook Tasks**

For notebook tasks, users configure:

- Notebook path

- Source location

- Compute

- Parameters

The notebook can come from:

- Workspace

- Git repository

This supports both interactive development and source-controlled deployments.

------------------------------------------------------------------------

**7. Job Clusters**

Each workflow task can execute on a **Job Compute Cluster**.

Benefits include:

- Automatically created when the workflow starts.

- Automatically terminated when the workflow completes or fails.

- Reduces infrastructure costs.

Job clusters are generally recommended for production workloads.

------------------------------------------------------------------------

**8. Task Parameters**

Each task can receive parameters.

Notebook parameters are typically created using:

dbutils.widgets

Workflow parameters populate these widgets automatically during execution.

------------------------------------------------------------------------

**9. Task Notifications**

Each task supports notifications such as:

- Success

- Failure

These alerts help monitor automated pipelines.

------------------------------------------------------------------------

**10. Retries**

Workflows support automatic retries.

If a task fails:

- Databricks can retry execution.

- The number of retries is configurable.

This improves reliability for transient failures.

------------------------------------------------------------------------

**11. Duration Thresholds**

Tasks can define:

- Warning thresholds

- Timeout limits

Example:

If a task exceeds **2 hours**, Databricks can automatically terminate it.

This prevents runaway jobs.

------------------------------------------------------------------------

**Job-Level Configuration**

The workflow also supports settings that apply to the **entire job** rather than individual tasks.

------------------------------------------------------------------------

**12. Scheduling**

Jobs can be scheduled using:

- Daily schedules

- Weekly schedules

- Custom intervals

- Cron expressions

This allows fully automated execution.

------------------------------------------------------------------------

**13. Job Parameters**

Unlike task parameters, **Job Parameters** are automatically available to every task within the workflow.

This eliminates the need to repeatedly define common parameters.

------------------------------------------------------------------------

**14. Job Notifications**

Notifications can also be configured globally for the job rather than individually for each task.

------------------------------------------------------------------------

**15. Permissions**

Workflow permissions determine who can:

- View jobs

- Run jobs

- Manage jobs

- Own jobs

These permissions support secure collaboration.

------------------------------------------------------------------------

**Advanced Settings**

**16. Queueing**

If compute resources are unavailable:

Queue Enabled:

- Job waits for available resources.

- Can wait up to 48 hours.

Queue Disabled:

- Job fails immediately.

Queueing is useful during periods of high cluster utilization.

------------------------------------------------------------------------

**17. Concurrent Runs**

Administrators can specify:

Maximum Concurrent Runs

This determines how many instances of the same job may execute simultaneously.

Example:

- 1 → Only one execution allowed.

- 5 → Five parallel executions permitted.

------------------------------------------------------------------------

**Workflow Design**

The instructor prepares several notebooks to build the workflow.

The planned workflow includes notebooks for:

- Determine current date

- Evaluate day of week

- Process employee data

These notebooks will later be connected using workflow dependencies.

------------------------------------------------------------------------

**Planned Workflow Logic**

Start\
│\
▼\
Get Current Date\
│\
▼\
Determine Day\
│\
▼\
Is Today Sunday?\
│\
┌─┴─────────────┐\
│ │\
Yes No\
│ │\
▼ ▼\
Process Data End Job\
│\
▼\
Write Department Tables

This demonstrates conditional branching inside a Databricks Workflow.

------------------------------------------------------------------------

**Workflow Components**

| **Component**   | **Purpose**                              |
|-----------------|------------------------------------------|
| Job             | Complete workflow                        |
| Task            | Individual processing step               |
| Job Cluster     | Temporary compute for workflow execution |
| Task Parameters | Input for individual tasks               |
| Job Parameters  | Shared inputs for all tasks              |
| Schedule        | Automates job execution                  |
| Notifications   | Success/failure alerts                   |
| Retry           | Automatic rerun after failures           |
| Queue           | Wait for available resources             |
| Concurrent Runs | Parallel job execution limit             |

------------------------------------------------------------------------

**Key Takeaways**

- **Databricks Workflows** provide a centralized way to orchestrate, schedule, and monitor multi-step data pipelines.

- A **Job** represents the complete workflow, while **Tasks** are the individual processing steps that make up the job.

- Workflows support a variety of task types, including notebooks, SQL, Python scripts, Delta Live Tables, dbt, conditional (If/Else) logic, and looping (For Each).

- **Job Compute Clusters** are automatically created when a workflow starts and terminated when it finishes, making them cost-efficient for production workloads.

- Parameters can be defined at both the **task level** and the **job level**, allowing notebooks to receive dynamic input through dbutils.widgets.

- Built-in features such as **scheduling**, **notifications**, **automatic retries**, **timeouts**, **queueing**, and **concurrent run limits** help make workflows reliable, scalable, and production-ready.

- The lesson lays the foundation for building more advanced workflow pipelines that combine conditional execution, parameter passing, and multiple interconnected notebooks.

# [README](./../../../README.md)
