# ANSWER 03 6

**What components are located in the Data Plane?**

A. Web UI, logs, and orchestration services\
**B. Customer data, Spark clusters, and processing workloads**\
C. Notebook configurations and cluster configurations\
D. User accounts and groups\
E. Metastore metadata and catalogs

**Correct Answer: B**

**The Most Important Databricks Architecture Concept**

For certification exams, the most heavily tested architecture concept is:

Databricks Architecture\
\
Control Plane\
│\
▼\
Data Plane

You should immediately memorize:

| **Control Plane** | **Data Plane**         |
|-------------------|------------------------|
| UI                | Customer Data          |
| Notebook Configs  | Spark Clusters         |
| Cluster Configs   | Compute Resources      |
| Job Configs       | Processing Workloads   |
| Logs              | Data Processing        |
| Orchestration     | Customer-Owned Storage |

------------------------------------------------------------------------

**Visual Architecture**

Databricks\
Control Plane\
│\
├── Web UI\
├── Notebook Configurations\
├── Cluster Configurations\
├── Job Configurations\
└── Logs & Orchestration\
\
│\
▼\
\
Customer Cloud Account\
Data Plane\
│\
├── Customer Data\
├── Spark Clusters\
└── Processing Workloads

------------------------------------------------------------------------

**Why B is Correct**

**B. Customer data, Spark clusters, and processing workloads ✅**

This is exactly what your notes state.

The Data Plane contains:

**Customer Data**

Examples:

sales.parquet\
customers.parquet\
transactions.csv

Stored in:

- AWS S3

- Azure Data Lake Storage

- Google Cloud Storage

------------------------------------------------------------------------

**Spark Clusters**

Examples:

Driver Node\
Worker Nodes\
Executors

These clusters perform actual computation.

------------------------------------------------------------------------

**Processing Workloads**

Examples:

df.read.parquet(...)\
df.groupBy(...)\
df.write.save(...)

ETL jobs, streaming jobs, machine learning workloads, and SQL workloads all run in the Data Plane.

------------------------------------------------------------------------

**Memory Trick**

Think:

Data Plane =\
Data + Compute

If something stores data or processes data, it belongs in the Data Plane.

------------------------------------------------------------------------

**Why A is Wrong**

**A. Web UI, logs, and orchestration services ❌**

These are Control Plane components.

Your notes explicitly state:

Control Plane manages:

- Web Application/UI

- Logs

- Orchestration Services

- Job Configurations

- Cluster Configurations

Example:

Control Plane\
│\
├── UI\
├── Logs\
└── Orchestration

The Control Plane manages operations.

It does not process customer data.

------------------------------------------------------------------------

**Exam Shortcut**

If you see:

UI\
Logs\
Orchestration\
Configurations

Think:

Control Plane

Not Data Plane.

------------------------------------------------------------------------

**Why C is Wrong**

**C. Notebook configurations and cluster configurations ❌**

These are also Control Plane components.

Your notes specifically state:

Control Plane stores:

- Notebook configurations

- Cluster configurations

Example:

Notebook Settings\
Cluster Settings\
Job Settings

These are instructions about how to run workloads.

They are not the workloads themselves.

**Think About It**

Configuration says:

Use 4 workers\
Use Runtime 14.3\
Use Auto Scaling

Actual processing says:

Read Data\
Transform Data\
Write Data

Configurations = Control Plane

Processing = Data Plane

------------------------------------------------------------------------

**Why D is Wrong**

**D. User accounts and groups ❌**

Users and groups are managed at the Databricks Account level.

Examples:

Data Engineers\
Analysts\
Data Scientists

These are identity and access management objects.

They are administrative resources, not compute resources.

------------------------------------------------------------------------

**Example**

User: John\
Group: Data Engineers

Neither stores data nor processes data.

Therefore they do not belong in the Data Plane.

------------------------------------------------------------------------

**Exam Tip**

If the answer contains:

Users\
Groups\
Permissions\
Roles

Think:

Administration

Not:

Data Plane

------------------------------------------------------------------------

**Why E is Wrong**

**E. Metastore metadata and catalogs ❌**

This is another common confusion.

A metastore contains:

Catalogs\
Schemas\
Tables\
Permissions\
Metadata

Example:

sales_catalog\
finance_catalog\
marketing_catalog

These are governance and metadata objects.

They describe data.

They are not the actual data.

------------------------------------------------------------------------

**Important Distinction**

Data Plane:

sales.parquet\
transactions.parquet

Metastore:

sales_catalog.sales.transactions

One stores the file.

One stores information about the file.

Those are different things.

------------------------------------------------------------------------

**The Fastest Way to Solve These Questions**

Ask:

**Does it process data?**

If YES:

Data Plane

Examples:

- Spark Clusters

- Workers

- Executors

- Customer Data

- ETL Jobs

------------------------------------------------------------------------

**Does it manage the platform?**

If YES:

Control Plane

Examples:

- UI

- Job Configurations

- Cluster Configurations

- Logs

- Orchestration

------------------------------------------------------------------------

**Certification-Level Takeaway**

Memorize this comparison:

| **Control Plane** | **Data Plane**  |
|-------------------|-----------------|
| UI                | Customer Data   |
| Logs              | Spark Clusters  |
| Orchestration     | Executors       |
| Notebook Configs  | Data Processing |
| Cluster Configs   | ETL Jobs        |
| Job Configs       | ML Workloads    |

The Data Plane is where:

✅ Data lives\
✅ Spark clusters run\
✅ Jobs execute\
✅ Processing occurs

The Control Plane is where:

✅ Databricks manages and orchestrates the platform

Therefore, **B. Customer data, Spark clusters, and processing workloads** is the correct answer. ✅

# [README](./../../../README.md)
