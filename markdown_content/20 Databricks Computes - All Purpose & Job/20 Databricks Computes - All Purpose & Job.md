# 20 Databricks Computes - All Purpose & Job

**Databricks Compute – All-Purpose Compute and Job Compute**

This lesson introduces **Databricks Compute (Clusters)**, explaining how compute resources execute notebooks, jobs, and SQL queries. It covers **All-Purpose Compute**, **Job Compute**, compute configuration, access modes, runtime versions, auto-scaling, permissions, and cluster policies.

**Key Topics Covered**

**1. What is Databricks Compute?**

A **Compute** (also called a **Cluster**) is the processing engine that executes code in Databricks.

A cluster consists of:

- **Driver Node**

  - Coordinates work.

  - Runs the Spark Driver.

- **Worker Nodes**

  - Execute Spark tasks.

  - Process data in parallel.

Driver\
│\
┌───────┴────────┐\
│ │\
Worker 1 Worker 2\
│ │\
└──── Process Data ────┘

Every notebook, SQL query, or job requires compute to execute.

**2. Types of Compute**

Databricks provides two primary compute types:

**All-Purpose Compute**

Used for:

- Interactive notebook development

- SQL exploration

- Testing

- Manual execution

Developers start and stop these clusters manually.

**Job Compute**

Used for:

- Scheduled jobs

- Production workflows

- Automated pipelines

Job Compute is created automatically when a job starts and terminated automatically when the job finishes.

**All-Purpose Compute**

**3. Creating a Cluster**

Creating an All-Purpose Compute requires configuring several options.

The most important include:

- Cluster Name

- Policy

- Cluster Type

- Access Mode

- Runtime Version

- Virtual Machine Type

- Auto Scaling

- Auto Termination

**4. Cluster Name**

The cluster name identifies the compute.

Example:

Demo Cluster

This helps users distinguish multiple clusters.

**5. Cluster Policies**

Policies define restrictions and defaults for compute creation.

Examples include:

- Unrestricted

- Personal Compute

- Shared Compute

- Power User Compute

- Legacy Shared Compute

Policies simplify cluster creation and enforce organizational standards.

**6. Single Node vs. Multi Node**

**Single Node**

- One Driver

- No Worker nodes

- Lower cost

- Good for development and testing

**Multi Node**

- One Driver

- One or more Workers

- Parallel processing

- Suitable for production workloads

**7. Access Modes**

Access Mode determines who can use the cluster and whether Unity Catalog is supported.

**Single User**

- Dedicated to one user

- Unity Catalog supported

- Uses that user's Azure credentials

**Shared**

- Multiple users

- Unity Catalog supported

- Best for collaborative environments

**No Isolation Shared**

- Multiple users

- Legacy mode

- Not Unity Catalog compatible

- Intended for Hive Metastore workloads

**8. Databricks Runtime (DBR)**

Databricks Runtime (DBR) is a preconfigured software image containing:

- Apache Spark

- Scala

- Python

- Delta Lake

- Optimizations

- Bug fixes

The lesson recommends selecting the latest **LTS (Long-Term Support)** release whenever possible.

**9. Photon**

Photon is Databricks' high-performance execution engine written in C++.

Benefits include faster performance for:

- ETL

- Batch processing

- Streaming

- SQL queries

- Data Science workloads

Enabling Photon increases DBU usage slightly but can significantly improve execution speed.

**10. Worker and Driver Types**

Users choose Azure Virtual Machine sizes based on workload requirements.

Examples include:

- General Purpose

- Memory Optimized

- Compute Optimized

Each VM type specifies:

- CPU cores

- Memory

- Performance characteristics

The Driver and Workers can use different VM types if needed.

**11. Auto Scaling**

Auto Scaling automatically adjusts the number of worker nodes.

Users configure:

- Minimum workers

- Maximum workers

Example:

Min Workers = 2\
Max Workers = 8

The cluster expands and contracts based on workload demands.

If Auto Scaling is disabled, the worker count remains fixed.

**12. Auto Termination**

One of the most important cost-saving settings is:

Terminate After

If the cluster remains idle for the configured time (for example, 30 minutes), Databricks automatically shuts it down.

This prevents unnecessary cloud costs.

**13. Tags**

Tags allow administrators to categorize clusters.

Example:

Owner = Ease with Data

Tags simplify:

- Cost reporting

- Resource organization

- Billing analysis

**14. Advanced Options**

Advanced cluster configuration includes:

- Spark Configuration

- Environment Variables

- Cluster Logging

- Init Scripts

For example, cluster logs can be stored in DBFS for troubleshooting.

**Cluster Monitoring**

**15. Libraries**

Clusters can automatically install libraries.

Supported library types include:

- JAR

- Python Wheel (.whl)

Libraries are attached to the cluster during startup.

**16. Event Log**

The Event Log records cluster events such as:

- Worker additions

- Worker removals

- Auto Scaling activity

Useful for diagnosing scaling behavior.

**17. Spark UI**

The Spark UI provides detailed execution information.

Developers use it to monitor:

- Jobs

- Stages

- Tasks

- Executors

- Performance

It is one of the primary debugging tools for Spark applications.

**18. Driver Logs**

Driver Logs include:

- Standard Output

- Standard Error

- Log4j logs

These logs help diagnose cluster and application issues.

**19. Cluster Metrics**

Metrics provide resource utilization statistics such as:

- CPU Usage

- Memory Usage

- Hardware metrics

- Spark metrics

- GPU metrics (when applicable)

These dashboards help identify bottlenecks and optimize cluster sizing.

**Cluster Permissions**

**20. Cluster Access Levels**

Clusters support three permission levels.

**Can Manage**

Allows users to:

- Edit cluster

- Delete cluster

- Manage configuration

**Can Restart**

Allows users to:

- Start cluster

- Stop cluster

Cannot modify configuration.

**Can Attach To**

Allows users to:

- Attach notebooks

- Execute code

Cannot start, stop, edit, or delete the cluster.

**Compute Policies**

Policies simplify cluster creation by preconfiguring settings.

Examples include:

| **Policy**            | **Description**                      |
|-----------------------|--------------------------------------|
| Personal Compute      | Single-user development cluster      |
| Shared Compute        | Multi-user Unity Catalog cluster     |
| Power User Compute    | Multi-user cluster with Auto Scaling |
| Legacy Shared Compute | Shared cluster using Hive Metastore  |

Policies also restrict available VM types and configuration options.

**Job Compute**

Unlike All-Purpose Compute, Job Compute:

- Is created automatically

- Runs a scheduled workflow

- Terminates automatically when finished

Workflow:

Workflow Starts\
│\
▼\
Create Job Cluster\
│\
▼\
Execute Job\
│\
▼\
Terminate Cluster

This minimizes infrastructure costs because compute exists only while the job is running.

**All-Purpose vs. Job Compute**

| **Feature**                   | **All-Purpose Compute** | **Job Compute** |
|-------------------------------|-------------------------|-----------------|
| Interactive development       | ✔                       | ✘               |
| Scheduled workflows           | Possible                | ✔               |
| Starts manually               | ✔                       | ✘               |
| Starts automatically          | ✘                       | ✔               |
| Stops automatically           | Optional                | ✔               |
| Best for development          | ✔                       | ✘               |
| Best for production pipelines | ✘                       | ✔               |

**Serverless Compute**

The lesson concludes by introducing **Serverless Compute**, which will be covered later.

Unlike traditional clusters, Serverless Compute:

- Requires no cluster configuration

- Automatically provisions compute resources

- Eliminates infrastructure management

- Allows users to focus solely on writing code

**Key Takeaways**

- A **Databricks Compute (Cluster)** provides the processing power required to execute notebooks, SQL queries, and workflows.

- Clusters consist of a **Driver** node that coordinates execution and one or more **Worker** nodes that perform distributed processing.

- **All-Purpose Compute** is intended for interactive development, while **Job Compute** is optimized for automated workflows by creating and terminating clusters automatically.

- **Access Modes** (Single User, Shared, and No Isolation Shared) determine who can use a cluster and whether it supports **Unity Catalog**.

- **Databricks Runtime (DBR)** packages Spark, Python, Scala, Delta Lake, and platform optimizations into a single managed runtime, with **LTS versions** recommended for stability.

- **Photon** is an optional high-performance execution engine that improves query and ETL performance at a modest additional DBU cost.

- Features such as **Auto Scaling**, **Auto Termination**, **Cluster Policies**, **Spark UI**, **Driver Logs**, and **Metrics** help optimize performance, simplify administration, and reduce cloud costs.

- **Serverless Compute** further simplifies cluster management by automatically provisioning compute resources, eliminating the need for manual cluster configuration.

# [README](./../../../README.md)
