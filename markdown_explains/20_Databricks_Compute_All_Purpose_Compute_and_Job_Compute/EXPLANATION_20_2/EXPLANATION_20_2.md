# EXPLANATION 20 2

**Question 1**

**What is the primary purpose of a Databricks Compute (Cluster)?**

**Correct Answer: B. To execute notebooks, SQL queries, and workflows**

**Explanation**

A Databricks Compute (cluster) provides the CPU, memory, and Spark runtime needed to process data. Without a running compute resource, notebooks cannot execute code.

A cluster is responsible for running:

- Python notebooks

- SQL queries

- Scala notebooks

- R notebooks

- Spark jobs

- Machine Learning workloads

- Streaming applications

- Databricks Workflows

Example:

df = spark.read.table("sales.transactions")\
display(df)

The notebook sends this work to the cluster, which performs the computation and returns the results.

**Real-world analogy**

Think of Databricks like a construction project:

- **Notebook** = The blueprint.

- **Cluster** = The construction crew.

- **Spark** = The tools and machinery.

Without the crew (cluster), the blueprint cannot be turned into a finished building.

**YouTube**

- **Databricks Clusters Explained**\
  https://www.youtube.com/results?search_query=Databricks+Clusters+Explained

- **Databricks Compute Tutorial**\
  https://www.youtube.com/results?search_query=Databricks+Compute+Tutorial

# [README](./../../../README.md)
