# ANSWER 03 7

**What is the relationship between the Control Plane and customer data?**

A. Customer data is copied to the Control Plane for processing.\
B. Customer data is stored only in the Control Plane.\
**C. Customer data remains in the customer's cloud account and does not move to the Control Plane.**\
D. Customer data is replicated to all workspaces through the Control Plane.\
E. Customer data is stored in Databricks-managed storage by default.

**Correct Answer: C**

**This Is One of the Most Important Databricks Security Concepts**

If you remember only one architecture security principle, remember this:

**Customer data stays in the customer's cloud account and does NOT move to the Databricks Control Plane.**

This is one of Databricks' core architectural and security design principles.

------------------------------------------------------------------------

**Visualizing the Architecture**

Databricks Control Plane\
│\
├── UI\
├── Notebook Configurations\
├── Job Configurations\
├── Cluster Configurations\
└── Orchestration\
\
│ Controls\
▼\
\
Customer Cloud Account\
(Data Plane)\
│\
├── Customer Data\
├── Spark Clusters\
└── Processing Workloads

Notice:

Control Plane = Management\
Data Plane = Data + Processing

The Control Plane tells the Data Plane what to do.

The Control Plane does NOT take ownership of the data.

------------------------------------------------------------------------

**Why C is Correct**

**C. Customer data remains in the customer's cloud account and does not move to the Control Plane. ✅**

This statement exactly matches your notes.

Your notes explicitly state:

"Customer data does NOT move to the control plane."

and

"Data stays in the customer's cloud account."

and

"Processing happens in customer-owned clusters."

This means:

AWS S3\
Azure Data Lake\
Google Cloud Storage

remain under the customer's cloud account.

The Spark clusters process the data there.

Databricks manages the platform, but does not move customer data into the Control Plane.

------------------------------------------------------------------------

**Simple Analogy**

Think of the Control Plane as a manager.

Manager\
│\
▼\
Workers perform the work

The manager gives instructions.

The workers handle the actual materials.

Similarly:

Control Plane\
│\
▼\
Data Plane processes data

------------------------------------------------------------------------

**Why A is Wrong**

**A. Customer data is copied to the Control Plane for processing. ❌**

This is the exact opposite of the architecture.

The Control Plane does not process customer data.

Processing occurs in:

Customer Cloud Account\
(Data Plane)

Example:

S3 Bucket\
↓\
Spark Cluster\
↓\
Transform Data

The data remains in the customer's environment.

If Databricks copied all customer data into the Control Plane:

- Security concerns would increase.

- Compliance concerns would increase.

- Data sovereignty concerns would increase.

Databricks intentionally avoids this model.

------------------------------------------------------------------------

**Exam Tip**

If an answer says:

Data moves into the Control Plane

It's almost always wrong.

------------------------------------------------------------------------

**Why B is Wrong**

**B. Customer data is stored only in the Control Plane. ❌**

This is even more incorrect.

Customer data is stored in:

- AWS S3

- Azure Data Lake Storage

- Google Cloud Storage

Examples:

sales.parquet\
transactions.parquet\
customers.parquet

These files reside in the customer's cloud account.

The Control Plane stores:

- Configurations

- Logs

- Job definitions

- Orchestration information

Not customer datasets.

------------------------------------------------------------------------

**Quick Check**

Ask yourself:

Where is the actual data?

Answer:

Data Plane

Never:

Control Plane

------------------------------------------------------------------------

**Why D is Wrong**

**D. Customer data is replicated to all workspaces through the Control Plane. ❌**

This sounds plausible but is incorrect.

Workspaces may share access to data through:

- Unity Catalog

- Shared Metastores

- Permissions

Example:

Metastore\
│\
┌─────┼─────┐\
▼ ▼ ▼\
Dev UAT Prod

What is shared?

Metadata\
Permissions\
Catalog Definitions

Not necessarily the physical data itself.

The Control Plane does not automatically replicate customer data across workspaces.

------------------------------------------------------------------------

**Common Confusion**

Students often confuse:

Sharing Metadata

with

Copying Data

These are very different concepts.

------------------------------------------------------------------------

**Why E is Wrong**

**E. Customer data is stored in Databricks-managed storage by default. ❌**

Your architecture notes emphasize:

The Data Plane resides in the customer's cloud account.

This means the customer owns the cloud storage.

Examples:

Customer AWS Account\
Customer Azure Subscription\
Customer GCP Project

The data remains there.

Databricks provides management and orchestration services.

It does not automatically move all customer data into Databricks-owned storage.

------------------------------------------------------------------------

**Exam Shortcut**

When you see:

Databricks-owned storage\
Databricks-managed storage\
Control Plane storage

Be cautious.

The architecture principle is:

Customer data remains in customer-controlled cloud resources.

------------------------------------------------------------------------

**The Key Distinction**

**Control Plane**

Responsible for:

UI\
Logs\
Configurations\
Orchestration\
Job Definitions

Question:

Does it store customer data?

Answer:

❌ No

------------------------------------------------------------------------

**Data Plane**

Responsible for:

Customer Data\
Spark Clusters\
Processing Workloads\
ETL Jobs\
Machine Learning Jobs

Question:

Does it process customer data?

Answer:

✅ Yes

------------------------------------------------------------------------

**Certification-Level Takeaway**

Memorize this statement exactly:

**Customer data remains in the customer's cloud account and does not move to the Databricks Control Plane.**

This is one of the most tested Databricks architecture and security concepts.

**Control Plane**

- UI

- Configurations

- Orchestration

- Management

**Data Plane**

- Customer Data

- Spark Clusters

- Processing

Therefore, **C. Customer data remains in the customer's cloud account and does not move to the Control Plane** is the correct answer. ✅

# [README](./../../../README.md)
