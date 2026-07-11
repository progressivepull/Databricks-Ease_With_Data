# 40 Serverless Compute for Notebooks Jobs DLT ML and Warehouses

**Serverless Compute for Notebooks, Jobs, DLT, ML, and SQL Warehouses**

This lesson introduces **Databricks Serverless Compute**, a fully managed compute service that eliminates the need to manually create, configure, and manage clusters. Instead of provisioning clusters yourself, Databricks automatically supplies, scales, and terminates compute resources for notebooks, jobs, Delta Live Tables (DLT), Machine Learning workloads, and SQL Warehouses.

------------------------------------------------------------------------

**1. What is Serverless Compute?**

Serverless Compute is a Databricks-managed compute service.

Instead of creating clusters manually:

Notebook\
\
↓\
\
Serverless Compute\
\
↓\
\
Databricks manages:\
• Cluster creation\
• Scaling\
• Maintenance\
• Termination

Developers simply attach Serverless Compute and run their workloads.

Databricks handles the infrastructure automatically.

------------------------------------------------------------------------

**2. Traditional Compute vs Serverless**

**Traditional Compute**

You must:

- Create clusters

- Choose VM sizes

- Configure autoscaling

- Start clusters

- Stop clusters

- Maintain clusters

------------------------------------------------------------------------

**Serverless Compute**

You only:

- Enable Serverless

- Attach it to the workload

- Run your code

Everything else is handled by Databricks.

------------------------------------------------------------------------

**3. Architecture Changes**

Traditional Databricks architecture contains:

Control Plane\
\
↓\
\
Data Plane\
\
↓\
\
Classic Compute

With Serverless:

Control Plane\
│\
Serverless Compute Plane\
│\
Customer Data Plane

Unlike classic clusters, Serverless Compute runs from a Databricks-managed compute plane while securely accessing customer data.

------------------------------------------------------------------------

**4. Classic Compute**

Classic Compute includes:

- All-Purpose Clusters

- Job Clusters

Characteristics:

- Customer-managed configuration

- Longer startup time

- Manual scaling configuration

These clusters run inside the customer's data plane.

------------------------------------------------------------------------

**5. Serverless Compute Plane**

Databricks maintains a fleet of pre-provisioned virtual machines.

Workflow:

Notebook\
\
↓\
\
Serverless Request\
\
↓\
\
Existing VM\
\
↓\
\
Job Starts

Because compute resources are already running, notebooks and jobs start within seconds instead of minutes.

------------------------------------------------------------------------

**6. Intelligent Scaling**

Serverless automatically:

- Scales up

- Scales down

- Optimizes resources

- Manages infrastructure

Developers no longer need to configure autoscaling policies manually.

------------------------------------------------------------------------

**7. Security Isolation**

Databricks isolates Serverless workloads.

Important behaviors:

- Compute is region-aware.

- Workloads run in the same region as the workspace whenever possible.

- Virtual machines used for one customer are not reused for another customer.

- Network isolation protects customer data.

This provides strong multi-tenant security.

------------------------------------------------------------------------

**8. Regional Availability**

Serverless is **not available in every cloud region**.

Before enabling Serverless:

- Verify your workspace region.

- Check Databricks' supported-region documentation.

If the workspace is in an unsupported region, Serverless options will not appear even if the feature is enabled.

**9. Enabling Serverless**

For Azure Databricks, Serverless is enabled by an **Account Administrator**.

Navigation:

Account Console\
\
↓\
\
Settings\
\
↓\
\
Feature Enablement\
\
↓\
\
Enable Serverless

Express Edition workspaces already have Serverless enabled by default.

------------------------------------------------------------------------

**10. Budget Policies**

Serverless introduces **Budget Policies**.

Purpose:

- Tag Serverless usage

- Track DBU costs

- Organize spending

- Support chargeback/showback

Example:

Budget Policy\
\
↓\
\
Tag\
\
↓\
\
Serverless Usage\
\
↓\
\
Cost Reports

Budget policies help organizations monitor Serverless consumption.

------------------------------------------------------------------------

**11. Budget Policy Permissions**

Users require permission to use a Budget Policy.

Permission levels include:

- Manager

- User

Administrators assign these permissions so users can apply the policy to notebooks, jobs, or pipelines.

------------------------------------------------------------------------

**12. Using Serverless in Notebooks**

Connecting Serverless is simple.

Workflow:

Notebook\
\
↓\
\
Connect\
\
↓\
\
Serverless\
\
↓\
\
Connected

Connection typically takes only a few seconds because the infrastructure is already running.

------------------------------------------------------------------------

**13. Supported Notebook Languages**

At the time of the lesson, Serverless notebooks support:

- Python

- SQL

Other notebook languages may be supported in the future.

------------------------------------------------------------------------

**14. Serverless Configuration**

Notebook configuration includes:

- REPL Memory

- Budget Policy

- Environment

- Python Libraries

- Logs

Users can customize these settings without managing the underlying cluster.

------------------------------------------------------------------------

**15. Memory Options**

Two memory profiles are demonstrated:

- Standard

- High Memory

These settings affect the notebook's Python REPL environment, not the underlying Spark cluster configuration.

**16. Library Support**

Serverless notebooks support installing Python packages.

Users can:

- Install pip libraries

- View installation logs

- Access Serverless logs

This enables custom Python environments without cluster management.

------------------------------------------------------------------------

**17. Query Performance Tools**

Serverless provides built-in performance information.

Users can view:

- Query Profile

- Execution statistics

- Performance metrics

These tools help analyze and optimize notebook execution.

------------------------------------------------------------------------

**18. Serverless Jobs**

Existing Workflows can be migrated from classic clusters.

Before:

Workflow\
\
↓\
\
All-Purpose Cluster

After:

Workflow\
\
↓\
\
Serverless

Every task automatically runs on Serverless without managing dedicated compute.

------------------------------------------------------------------------

**19. Serverless DLT Pipelines**

Delta Live Tables also support Serverless.

Benefits include:

- Automatic infrastructure

- Incremental refresh

- Simplified configuration

- Better operational efficiency

Enabling Serverless on a DLT pipeline removes the need to manage pipeline compute manually.

------------------------------------------------------------------------

**20. Cost Model**

Unlike traditional clusters, Serverless uses a simplified pricing model.

You pay:

- Databricks DBUs

The Serverless price already includes:

- Infrastructure

- Virtual machines

- Cluster management

This means you no longer receive separate VM charges from the cloud provider for Serverless compute.

------------------------------------------------------------------------

**21. Automatic Termination**

Serverless automatically shuts down when idle.

Behavior:

Idle\
\
↓\
\
Auto Terminate

Users may also terminate Serverless sessions manually from the notebook interface.

------------------------------------------------------------------------

**22. Pay-as-You-Go**

Serverless follows a **pay-as-you-go** model.

You are billed only for the time the Serverless compute is actively used.

This can reduce costs for workloads with intermittent or unpredictable usage.

------------------------------------------------------------------------

**23. Serverless Capabilities**

Serverless can be used for:

- Notebooks

- Workflows (Jobs)

- Delta Live Tables (DLT)

- Machine Learning workloads

- Databricks SQL Warehouses

This provides a consistent managed compute experience across multiple Databricks services.

------------------------------------------------------------------------

**Classic Compute vs Serverless**

| **Feature**         | **Classic Compute**       | **Serverless Compute** |
|---------------------|---------------------------|------------------------|
| Cluster Creation    | Manual                    | Automatic              |
| Scaling             | User configured           | Automatic              |
| Startup Time        | Minutes                   | Seconds                |
| VM Management       | Customer                  | Databricks             |
| Infrastructure Cost | Separate cloud VM charges | Included in DBUs       |
| Auto Termination    | Configurable              | Automatic              |
| Cluster Maintenance | Customer                  | Databricks             |

------------------------------------------------------------------------

**Best Practices**

- Use **Serverless Compute** whenever it is available to reduce operational overhead and speed up workload startup.

- Verify that your **workspace region supports Serverless** before enabling the feature.

- Create and assign **Budget Policies** so Serverless costs can be tracked and allocated accurately.

- Use Serverless for **notebooks, jobs, and DLT pipelines** to eliminate manual cluster management and benefit from automatic scaling.

- Remember that Serverless notebooks currently support **Python and SQL**.

- Take advantage of **automatic termination** and the **pay-as-you-go** pricing model to minimize costs for intermittent workloads.

# [README](./../../../README.md)
