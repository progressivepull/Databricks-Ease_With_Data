# ANSWER 40 3

**Question 3**

**How does the Serverless Compute architecture differ from Classic Compute?**

**A. Serverless runs entirely inside the customer's data plane using customer-managed clusters.** ❌ Incorrect

- That's closer to Classic Compute.

- Serverless compute is **Databricks-managed**.

**B. Serverless uses a Databricks-managed compute plane that securely accesses customer data.** ✅ Correct

- Databricks owns and manages the compute.

- The compute securely connects to customer data.

- Customers don't manage clusters.

**C. Serverless requires a dedicated cluster for every notebook session.** ❌ Incorrect

- Serverless provisions compute automatically.

- Users don't create dedicated clusters.

**D. Classic Compute and Serverless use the exact same infrastructure architecture.** ❌ Incorrect

- They use different architectures.

- Classic → customer-managed compute.

- Serverless → Databricks-managed compute.

**E. Serverless removes the Databricks Control Plane entirely.** ❌ Incorrect

- The Control Plane still exists.

- It orchestrates jobs, notebooks, authentication, and management.

**Key Concept**

Classic Compute

Customer

├── Data

└── Spark Clusters

Serverless

Customer

│

Data

▲

Secure Access

│

Databricks Managed Compute

# [README](./../../../README.md)
