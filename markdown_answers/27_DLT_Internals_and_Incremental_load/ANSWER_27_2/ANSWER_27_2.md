# ANSWER 27 2

**Question 2**

**What is created each time a Delta Live Tables pipeline executes?**

**A. A new Unity Catalog metastore ❌ Incorrect**

- A metastore is a shared metadata repository.

- Pipelines do **not** create new metastores.

------------------------------------------------------------------------

**B. A Delta Lake backup copy ❌ Incorrect**

- DLT does not automatically create backups during every execution.

- Delta Lake provides features like Time Travel, but that is different from creating backup copies.

------------------------------------------------------------------------

**C. An Update containing execution status, logs, metrics, and Spark UI information ✅ Correct**

Every pipeline run creates an **Update**.

An Update records:

- execution status

- success/failure

- logs

- metrics

- Spark UI information

- pipeline history

Think of an Update as a **run history record**.

Pipeline Run

↓

Update

├── Logs

├── Metrics

├── Status

├── Spark UI

└── History

------------------------------------------------------------------------

**D. A new Databricks workspace ❌ Incorrect**

- A workspace is an entire development environment.

- Pipelines run inside an existing workspace.

------------------------------------------------------------------------

**E. A second pipeline for disaster recovery ❌ Incorrect**

- DLT does not duplicate pipelines automatically.

------------------------------------------------------------------------

**Why C is correct**

Each execution generates an **Update**, providing detailed information for monitoring, debugging, and auditing pipeline runs.

------------------------------------------------------------------------

# [README](./../../../README.md)
