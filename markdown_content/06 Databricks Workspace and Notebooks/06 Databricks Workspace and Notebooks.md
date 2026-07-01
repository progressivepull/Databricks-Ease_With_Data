# 06 Databricks Workspace and Notebooks

**Workspace and Notebooks**

This lesson introduces the **Databricks Workspace**, explains how notebooks are organized, demonstrates creating a notebook, launching a compute cluster, running Python and SQL code, and highlights collaboration features available within Databricks notebooks.

**Key Topics Covered**

**1. Databricks Workspace Overview**

The Databricks Workspace is the primary development environment where users create and manage their work.

Depending on a user's permissions, the workspace may include personas such as:

- SQL

- Data Engineering

- Machine Learning

- Data Science

Workspace Administrators control which personas and features each user can access based on their role.

**2. Workspace Organization**

Databricks organizes workspace content using folders.

Each user automatically receives a personal workspace folder where they can store artifacts such as:

- Notebooks

- Queries

- Dashboards

- MLflow Experiments

- Files

Creating folders helps organize projects and notebooks.

**3. Creating a Notebook**

The lesson demonstrates creating a notebook by:

1.  Creating a new folder.

2.  Selecting **Create → Notebook**.

3.  Renaming the notebook.

A notebook serves as an interactive development environment for writing code, documentation, and visualizations.

**4. Supported Notebook Languages**

Databricks notebooks support multiple programming languages:

- Python

- SQL

- Scala

- R

Although a notebook has a default language, multiple languages can be used within the same notebook.

**5. Compute Is Required**

A notebook cannot execute code until it is attached to a **Compute** resource (cluster).

Initially, no compute exists, so one must be created before running code.

**6. Creating a Single Node Compute Cluster**

The lesson creates a simple **Single Node Compute**.

Configuration includes:

- Single Node mode

- Single User access

- Databricks Runtime

- General Purpose virtual machine

- Photon disabled

- Auto Termination set to **10 minutes**

Auto termination is emphasized as an important cost-saving feature because idle clusters automatically shut down, preventing unnecessary Azure charges.

**7. Connecting a Notebook to Compute**

After the compute starts:

- Attach the notebook to the cluster.

- A green status indicator confirms the compute is running.

- The notebook is now ready to execute code.

**8. Spark Session**

Every Databricks notebook automatically provides a **Spark Session**.

Typing:

spark

shows the existing Spark session without requiring manual creation.

**9. Creating a Spark DataFrame**

The lesson creates a simple DataFrame using:

spark.range(0,10)

This generates values from **0 through 9** and demonstrates that Spark is running successfully.

**10. Running Multiple Languages with Magic Commands**

Databricks supports multiple languages inside the same notebook using **Magic Commands**.

Examples include:

- %python

- %sql

- %sh

The lesson demonstrates:

**SQL**

%sql\
SHOW DATABASES

which displays the available Hive Metastore database.

**Shell**

%sh\
ls -ltr

which executes Linux shell commands directly from the notebook.

Magic commands allow users to switch languages without creating multiple notebooks.

**11. Hive Metastore**

Since Unity Catalog has not yet been configured, the notebook accesses the default **Hive Metastore**, which contains the default database.

Later lessons replace this with Unity Catalog.

**12. Markdown (Text) Cells**

Notebooks contain two types of cells:

**Code Cells**

- Execute Python, SQL, Scala, or R code.

**Markdown (Text) Cells**

- Add documentation

- Create titles

- Explain notebook logic

- Improve readability

Markdown cells do not execute code—they provide documentation alongside the code.

**13. Collaboration Features**

Databricks notebooks are collaborative.

Multiple users can work in the same notebook simultaneously.

Features include:

- Comments

- Shared editing

- Collaboration between team members

Comments allow developers to leave notes or request changes without modifying code.

**14. Version History**

Databricks automatically maintains notebook version history.

Users can:

- View previous versions

- Restore earlier versions

- Track notebook changes over time

This provides built-in version management.

**15. Variable Explorer**

The Variable Explorer displays variables currently stored in notebook memory.

Examples include:

- Spark DataFrames

- Python variables

- SQL DataFrames

This helps users inspect notebook state during development.

**16. Libraries**

The notebook interface also contains a **Libraries** section.

Libraries allow additional software packages to be installed on a compute cluster.

The lesson notes this topic will be covered in more detail later.

**17. Sharing Notebooks**

Notebooks can be shared with other users.

Permissions determine who can:

- View

- Edit

- Execute

This enables collaboration across teams such as:

- Data Engineers

- Data Scientists

- Data Analysts

- Business Analysts

**18. Terminating Compute**

After finishing work, the compute cluster should be terminated.

Benefits include:

- Stops Azure Virtual Machines

- Prevents unnecessary cloud charges

- Frees compute resources

The instructor emphasizes always stopping compute when it is no longer needed.

**Overall Workflow**

1.  Open the Databricks Workspace.

2.  Create a project folder.

3.  Create a notebook.

4.  Create a Single Node Compute cluster.

5.  Connect the notebook to the compute.

6.  Execute Python code using Spark.

7.  Execute SQL using %sql.

8.  Execute shell commands using %sh.

9.  Use Markdown for documentation.

10. Collaborate through comments and version history.

11. Terminate the compute cluster to save costs.

**Key Takeaways**

- The **Databricks Workspace** is where users create and organize notebooks and other development artifacts.

- Notebooks support **Python, SQL, Scala, and R**, and multiple languages can be combined using **Magic Commands**.

- Code execution requires attaching the notebook to a **Compute** cluster.

- Databricks automatically provides a **Spark Session**, making Spark immediately available.

- **Markdown cells** document notebooks, while **code cells** execute programs.

- Built-in features such as **comments**, **version history**, and the **Variable Explorer** support collaboration and development.

- Always enable **Auto Termination** and manually terminate compute when finished to reduce Azure infrastructure costs.

# [README](./../../../README.md)
