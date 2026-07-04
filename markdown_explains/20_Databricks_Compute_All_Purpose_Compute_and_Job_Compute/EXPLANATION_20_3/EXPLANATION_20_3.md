# EXPLANATION 20 3

**Question 2**

**Which component of a Databricks cluster is responsible for coordinating work and running the Spark Driver?**

**Correct Answer: C. Driver Node**

**Explanation**

Every Spark cluster contains:

- **Driver Node**

- **Worker Nodes**

The **Driver Node**:

- Runs the Spark Driver process.

- Executes your notebook code.

- Plans Spark jobs.

- Coordinates worker nodes.

- Collects results.

The **Worker Nodes**:

- Store partitions of data.

- Execute Spark tasks.

- Perform distributed computations.

Diagram:

Notebook\
│\
▼\
Driver Node\
│\
├── Worker 1\
├── Worker 2\
├── Worker 3\
└── Worker 4

The Driver acts like a project manager, while the Workers perform the actual processing.

**YouTube**

- **Spark Driver vs Worker Explained**\
  https://www.youtube.com/results?search_query=Spark+Driver+vs+Worker

- **Apache Spark Architecture**\
  https://www.youtube.com/results?search_query=Apache+Spark+Architecture

# [README](./../../../README.md)
