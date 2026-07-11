# ANSWER 39 3

**Question 3**

**Which Delta Sharing mode should be used when the recipient does not use Databricks?**

**A. Workspace Sharing ❌ Incorrect**

- Workspace Sharing is intended for Databricks workspaces.

**B. Internal Sharing ❌ Incorrect**

- Not an official Delta Sharing mode.

**C. Open Sharing ✅ Correct**

Open Sharing is designed for recipients outside Databricks.

Examples include:

- Pandas

- Apache Spark

- Power BI

- Tableau

- Excel (through supported connectors)

- Other analytics platforms

Example:

Databricks

│

▼

Open Sharing

│

▼

Python

Power BI

Spark

Tableau

**D. Cross-Metastore Sharing ❌ Incorrect**

- Not one of the Delta Sharing modes.

**E. Live Replication ❌ Incorrect**

- Replication copies data.

- Open Sharing accesses live data.

**Why C is correct**

Open Sharing enables organizations that do not use Databricks to securely access shared Delta data.

# [README](./../../../README.md)
