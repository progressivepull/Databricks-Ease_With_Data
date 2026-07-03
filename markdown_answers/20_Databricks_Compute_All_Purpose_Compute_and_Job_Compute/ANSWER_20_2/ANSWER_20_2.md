# ANSWER 20 2

**Question 2**

**Which component of a Databricks cluster is responsible for coordinating work and running the Spark Driver?**

**A. Worker Node** ❌ Incorrect

- Worker nodes perform computations assigned by the driver.

- They do **not** coordinate the cluster.

**B. Executor Node** ❌ Incorrect

- Executors run on worker nodes.

- They execute tasks but don't coordinate them.

**C. Driver Node** ✅ Correct

The Driver Node is the **brain** of the cluster.

Responsibilities:

- Runs Spark Driver

- Creates execution plans

- Sends work to workers

- Collects results

- Maintains Spark session

Architecture:

Driver Node\
\
↓\
\
Worker 1\
\
Worker 2\
\
Worker 3

**D. Photon Engine** ❌ Incorrect

- Photon speeds execution.

- It isn't the coordinator.

**E. SQL Warehouse** ❌ Incorrect

- SQL Warehouses are separate compute resources.

**Memory Trick**

Driver

↓

Directs

Workers

# [README](./../../../README.md)
