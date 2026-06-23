# EXPLANATION 03 5

**What Does "Managed in the Databricks Control Plane" Mean?**

To understand this concept, first understand that Databricks is divided into **two major planes**:

Databricks Platform\
│\
├── Control Plane\
└── Compute Plane (Data Plane)

------------------------------------------------------------------------

**1. Control Plane**

The **Control Plane** is managed by Databricks.

It contains the services that control, coordinate, and manage your Databricks environment.

Think of it as the **brain** of Databricks.

**The Control Plane Handles:**

- Workspace management

- Notebook metadata

- Job scheduling

- Cluster configuration

- User authentication

- Permissions

- Unity Catalog metadata

- Monitoring and logging

- APIs

Example:

User clicks "Create Cluster"\
↓\
Control Plane receives request\
↓\
Control Plane provisions cluster

The Control Plane makes decisions but does not perform the heavy computation.

------------------------------------------------------------------------

**2. Compute Plane (Data Plane)**

The **Compute Plane** is where the actual work happens.

Think of it as the **muscle** of Databricks.

**The Compute Plane Handles:**

- Running Spark jobs

- Processing data

- Executing notebooks

- Reading/writing files

- Machine learning training

Example:

Spark Job\
↓\
Runs on Compute Plane\
↓\
Processes 1 TB of data

------------------------------------------------------------------------

**Example Analogy**

Imagine a restaurant:

**Control Plane = Manager**

The manager:

- Takes orders

- Assigns tasks

- Schedules workers

- Tracks inventory

**Compute Plane = Kitchen Staff**

The kitchen:

- Cooks food

- Performs the actual work

Manager → Control Plane\
Kitchen → Compute Plane

------------------------------------------------------------------------

**What Is Managed in the Databricks Control Plane?**

Common exam question:

Which components are managed in the Databricks Control Plane?

**Examples**

**Workspace Metadata**

Workspace Names\
Folder Structure\
Notebook Metadata

Stored in the Control Plane.

------------------------------------------------------------------------

**User Accounts**

Users\
Groups\
Permissions

Managed in the Control Plane.

------------------------------------------------------------------------

**Cluster Definitions**

The configuration is stored in the Control Plane:

Cluster Name\
Node Type\
Spark Version\
Autoscaling Settings

The actual cluster runs in the Compute Plane.

------------------------------------------------------------------------

**Job Definitions**

Run ETL Daily at 2 AM

The schedule is stored in the Control Plane.

------------------------------------------------------------------------

**Unity Catalog Metadata**

Unity Catalog stores:

Catalogs\
Schemas\
Tables\
Permissions\
Lineage

This metadata is managed through the Control Plane.

------------------------------------------------------------------------

**What Is NOT Managed in the Control Plane?**

**Actual Data**

Example:

sales.parquet\
customer.csv\
delta tables

Stored in:

- Amazon S3

- Azure Data Lake Storage

- Google Cloud Storage

Not in the Control Plane.

------------------------------------------------------------------------

**Spark Execution**

df.count()

Runs in the Compute Plane.

------------------------------------------------------------------------

**Cluster Compute Resources**

Actual machines:

EC2 Instances\
Azure VMs\
GCE VMs

Exist in the Compute Plane.

------------------------------------------------------------------------

**Exam Trick**

Questions often ask:

Is this stored in the Control Plane or Compute Plane?

| **Item**               | **Control Plane** | **Compute Plane** |
|------------------------|-------------------|-------------------|
| Users                  | ✅                | ❌                |
| Permissions            | ✅                | ❌                |
| Workspace Metadata     | ✅                | ❌                |
| Unity Catalog Metadata | ✅                | ❌                |
| Job Definitions        | ✅                | ❌                |
| Cluster Configuration  | ✅                | ❌                |
| Spark Processing       | ❌                | ✅                |
| Data Files             | ❌                | ✅                |
| ML Training            | ❌                | ✅                |

------------------------------------------------------------------------

**Easy Memory Trick**

**Control Plane = Control**

Ask yourself:

Does it control or manage something?

If yes:

✅ Control Plane

Examples:

- Metadata

- Governance

- Permissions

- Users

- Workspace settings

------------------------------------------------------------------------

**Compute Plane = Compute**

Ask yourself:

Does it process data?

If yes:

✅ Compute Plane

Examples:

- Spark jobs

- SQL queries

- Machine learning

- ETL processing

------------------------------------------------------------------------

**Certification Definition**

**Managed in the Databricks Control Plane** means:

The object's metadata, configuration, governance, security, or orchestration is stored and managed by Databricks rather than being used for actual data processing.

**Remember:**

Control Plane\
= Metadata + Governance + Management\
\
Compute Plane\
= Data Processing + Execution

This distinction is heavily tested in Databricks Fundamentals, Data Engineer Associate, and Unity Catalog certification exams.

------------------------------------------------------------------------

Here are some strong YouTube resources for understanding **what is managed in the Databricks Control Plane** and the difference between the **Control Plane** and **Compute/Data Plane**:

**1. Databricks High Level Architecture \| Control Plane & Data Plane**

🎥 <https://www.youtube.com/watch?v=_2ZGN_Y6M2c>

Why watch:

- Explains Databricks architecture from the ground up.

- Covers Databricks Account, Workspace, Control Plane, and Data Plane.

- Good for certification exam preparation.

------------------------------------------------------------------------

**2. Azure Databricks Architecture Explained \| Control Plane vs Data Plane**

🎥 <https://www.youtube.com/watch?v=QLc38GA9UHE>

Why watch:

- Clear visual explanation of what belongs in the Control Plane versus the Data Plane.

- Covers workspaces, clusters, notebooks, and Spark execution.

------------------------------------------------------------------------

**3. Databricks Architecture Explained in 30 Seconds**

🎥 <https://www.youtube.com/watch?v=yKQJVjofajw>

Why watch:

- Very short overview.

- Explains the key exam concept that the **Control Plane is managed by Databricks**, while your data remains in your cloud account.

------------------------------------------------------------------------

**4. Databricks Architecture – How It Really Works**

🎥 <https://www.youtube.com/watch?v=9yKecTXW2pY>

Why watch:

- Covers Accounts, Workspaces, Unity Catalog, Control Plane, and Compute Plane.

- Excellent conceptual explanation for beginners.

------------------------------------------------------------------------

**5. Azure Databricks Series: Control Plane vs Data Plane**

🎥 <https://www.youtube.com/watch?v=xJrgPFfGy7Y>

Why watch:

- Detailed discussion of:

  - Authentication

  - Cluster management

  - Job scheduling

  - Monitoring and logging

- These are all examples of services managed in the Control Plane.

------------------------------------------------------------------------

**Certification Exam Cheat Sheet**

**Managed in the Databricks Control Plane ✅**

Users\
Groups\
Permissions\
Workspace Metadata\
Notebook Metadata\
Job Definitions\
Cluster Configurations\
Unity Catalog Metadata\
Data Lineage\
Auditing Information\
Monitoring & Logging

**Managed in the Compute (Data) Plane ✅**

Spark Processing\
SQL Query Execution\
Machine Learning Training\
ETL Jobs\
Actual Data Files\
Tables Stored in S3/ADLS/GCS

**Memory Trick**

Control Plane = Control\
\
Metadata\
Governance\
Security\
Management

Compute Plane = Compute\
\
Processing\
Execution\
Data Operations

This distinction—**metadata and governance in the Control Plane, data processing in the Compute Plane**—is one of the most frequently tested Databricks architecture concepts.

# [README](./../../../README.md)
