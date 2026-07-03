# ANSWER 19 1

**Question 1**

**What is the primary purpose of the parent notebook in the lesson?**

**A. To create Delta tables directly** ❌ Incorrect

- A parent notebook **can** create Delta tables, but that is not its primary role in this lesson.

- In this workflow, the child notebook performs the data processing and table creation.

**B. To read CSV files and filter employee data** ❌ Incorrect

- Those tasks belong to the child notebook.

- The parent notebook orchestrates the workflow rather than processing data.

**C. To pass parameters, execute the child notebook, and receive returned results** ✅ Correct

The parent notebook acts like a **manager**.

Its responsibilities are:

1.  Create parameter values.

2.  Pass them to the child notebook.

3.  Wait for the child notebook to finish.

4.  Receive the returned status or result.

Example:

Parent Notebook\
\
↓\
\
Pass Department = Sales\
\
↓\
\
Run Child Notebook\
\
↓\
\
Receive "SUCCESS"

Typical code:

result = dbutils.notebook.run(\
"/ETL/ChildNotebook",\
300,\
{"department": "Sales"}\
)

**D. To create Unity Catalog objects** ❌ Incorrect

- Unity Catalog objects are unrelated to notebook orchestration.

**E. To manage Spark clusters** ❌ Incorrect

- Cluster management is handled elsewhere.

------------------------------------------------------------------------

**Memory Trick**

Parent Notebook

↓

Controls Workflow

------------------------------------------------------------------------

# [README](./../../../README.md)
