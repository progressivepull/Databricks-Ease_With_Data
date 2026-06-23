# ANSWER 03 5

**Which of the following is managed in the Databricks Control Plane?**

A. Customer data files\
B. Spark executors\
C. Data processing workloads\
**D. Notebook configurations and job configurations**\
E. Raw data storage accounts

**Correct Answer: D**

**Key Concept to Remember**

The easiest way to answer this question is to remember:

**Control Plane = Management & Orchestration**

Managed by Databricks:

- Web UI

- Notebook configurations

- Cluster configurations

- Job configurations

- Logs

- Orchestration services

**Data Plane = Data & Compute**

Located in the customer's cloud account:

- Customer data

- Spark clusters

- Spark executors

- Data processing workloads

- Storage accounts

Think:

**Control Plane = "Manage"**\
**Data Plane = "Process"**

**Option A: Customer Data Files ❌ Wrong**

Customer data files are the actual business data being analyzed.

Examples:

- CSV files

- Parquet files

- Delta tables

- Images

- JSON files

These remain inside the customer's cloud account for security reasons.

Since customer data never moves to the Databricks Control Plane, this cannot be correct.

**Why wrong?**

- Customer data resides in the **Data Plane**

- Databricks only manages metadata and orchestration

**Option B: Spark Executors ❌ Wrong**

Spark executors are worker processes that perform computations.

Example:

- Reading data

- Running transformations

- Writing results

Executors run on Spark clusters deployed in the customer's cloud account.

**Why wrong?**

- Executors perform actual compute work

- Compute resources belong to the **Data Plane**

- Control Plane only manages cluster configuration, not execution

**Option C: Data Processing Workloads ❌ Wrong**

A data processing workload is the actual execution of code.

Examples:

- ETL jobs

- Data transformations

- Machine learning training

- Streaming jobs

These jobs run on customer-owned clusters.

**Why wrong?**

- Processing happens where the data lives

- Workloads execute in the **Data Plane**

- Control Plane only schedules and orchestrates them

A useful distinction:

| **Control Plane**     | **Data Plane**  |
|-----------------------|-----------------|
| Job Configuration     | Job Execution   |
| Cluster Configuration | Cluster Runtime |
| Orchestration         | Processing      |

**Option D: Notebook Configurations and Job Configurations ✅ Correct**

This is exactly what the Control Plane manages.

Examples:

- Notebook settings

- Job schedules

- Job definitions

- Cluster settings

- Workspace metadata

The Control Plane stores and orchestrates these configurations.

**Why correct?**

- These are management objects

- They define *how* work should run

- They do not contain customer data

- Databricks explicitly manages them in the Control Plane

**Option E: Raw Data Storage Accounts ❌ Wrong**

Storage accounts are cloud resources owned by the customer.

Examples:

- Amazon S3 buckets

- Azure Data Lake Storage (ADLS)

- Google Cloud Storage (GCS)

These storage locations hold the actual data.

**Why wrong?**

- Storage accounts contain customer data

- They exist in the customer's cloud environment

- Therefore they belong to the **Data Plane**

**Exam Tip**

When you see a Databricks architecture question, ask:

**Is it managing something?**

➡️ Control Plane

Examples:

- UI

- Jobs

- Notebook configurations

- Cluster configurations

- Logs

**Is it storing or processing data?**

➡️ Data Plane

Examples:

- Data files

- Storage accounts

- Spark clusters

- Executors

- ETL workloads

Using this rule, **D** is the only option that clearly belongs to the **Control Plane**.

# [README](./../../../README.md)
