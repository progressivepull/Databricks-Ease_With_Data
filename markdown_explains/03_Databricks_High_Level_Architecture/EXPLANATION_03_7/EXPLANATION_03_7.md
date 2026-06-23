# EXPLANATION 03 7

In Databricks, **Control Plane** and **Customer Data (Data Plane)** are separated for security and management.

**Simple Analogy**

Imagine a corporate office building:

- **Control Plane** = The management office

  - Keeps schedules

  - Assigns work

  - Manages employees and permissions

  - Doesn't store the company's sensitive documents

- **Customer Data Plane** = The secure records room

  - Stores actual business documents

  - Processes sensitive information

  - Access is tightly controlled

------------------------------------------------------------------------

**Control Plane**

The Databricks-managed environment.

It handles:

- Workspace UI

- Notebook metadata

- Job scheduling

- Cluster management

- Authentication and authorization

- APIs

- Monitoring and logging

Think of it as the **brain** of Databricks.

Example:

- You click **Run Notebook**

- The control plane receives the request

- It starts or uses a cluster

- It sends instructions to the data plane

The control plane typically runs in Databricks-managed cloud accounts.

------------------------------------------------------------------------

**Customer Data Plane**

The cloud resources in **your AWS/Azure/GCP account**.

It contains:

- Clusters (compute)

- Spark executors

- Storage access

- Processing of your datasets

Think of it as the **workers and machinery**.

Example:

- Your sales data is stored in S3, ADLS, or GCS

- Spark reads the data

- Transformations run on cluster nodes

- Results are written back to your storage

The actual data processing occurs here.

------------------------------------------------------------------------

**Request Flow**

1.  User opens Workspace

2.  Control Plane authenticates user

3.  User runs notebook

4.  Control Plane creates/manages cluster

5.  Cluster in Customer Data Plane reads data

6.  Processing occurs in Customer Data Plane

7.  Results returned to user

User\
\|\
v\
Control Plane\
(Workspace, Jobs, Permissions)\
\|\
v\
Customer Data Plane\
(Clusters, Spark, Storage)\
\|\
v\
Customer Data

------------------------------------------------------------------------

**What is Customer Data?**

Customer data includes:

- Tables

- CSV files

- JSON files

- Delta tables

- Images

- Logs

- ML datasets

- Query results

Examples:

- IRS tax records

- Banking transactions

- Retail sales data

- Healthcare records

These remain in your cloud environment and are processed by clusters in your data plane.

------------------------------------------------------------------------

**Certification Interview Answer**

**Control Plane** manages Databricks services such as workspaces, job orchestration, cluster management, and security.\
**Customer Data Plane** runs in the customer's cloud account and contains the compute resources that access, process, and store customer data. The separation improves security, governance, and scalability.

------------------------------------------------------------------------

Here are some YouTube videos that specifically explain **Databricks Control Plane, Data Plane, and Customer Data**:

**1. Databricks Architecture Explained – Control Plane vs Data Plane**

🔗 https://www.youtube.com/results?search_query=Databricks+control+plane+vs+data+plane

Topics:

- Control Plane

- Customer Data Plane

- Security boundaries

- Cluster management

- Data processing flow

------------------------------------------------------------------------

**2. Databricks Account, Workspace, Control Plane and Data Plane Architecture**

🔗 https://www.youtube.com/results?search_query=Databricks+architecture+control+plane+data+plane

Topics:

- Databricks account architecture

- Workspaces

- Control plane responsibilities

- Customer-managed cloud resources

------------------------------------------------------------------------

**3. Azure Databricks Architecture Explained**

🔗 https://www.youtube.com/results?search_query=Azure+Databricks+architecture+control+plane+data+plane

Topics:

- Azure Databricks deployment

- Microsoft-managed control plane

- Customer subscription data plane

- Networking and security

------------------------------------------------------------------------

**4. Databricks Fundamentals – Architecture Deep Dive**

🔗 https://www.youtube.com/results?search_query=Databricks+fundamentals+architecture+deep+dive

Topics:

- Workspace architecture

- Compute architecture

- Data access patterns

- Unity Catalog integration

------------------------------------------------------------------------

**Official Databricks Documentation (Highly Recommended)**

**Control Plane and Compute Plane Architecture**\
🔗 <https://docs.databricks.com/en/getting-started/overview.html>

**Databricks Architecture**\
🔗 https://docs.databricks.com/en/getting-started/concepts.html

------------------------------------------------------------------------

**30-Second Interview Answer**

**Control Plane**

- Managed by Databricks.

- Hosts the Workspace UI, job scheduler, cluster manager, APIs, and permissions.

- Acts as the "brain."

**Customer Data Plane**

- Runs in the customer's AWS/Azure/GCP account.

- Hosts clusters and processes data.

- Stores and accesses customer data.

- Acts as the "workers."

**Key Point:** Customer data is processed in the **customer data plane**, while the **control plane** manages and orchestrates the environment. This separation improves security and governance.

# [README](./../../../README.md)
