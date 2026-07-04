# EXPLANATION 22 3

**Question 2**

**In Databricks Workflows, what is the relationship between a Job and a Task?**

**Correct Answer: B. A Job is a complete workflow composed of one or more Tasks.**

**Explanation**

Think of a **Job** as the complete project and each **Task** as an individual step.

Example:

Daily Employee Pipeline (Job)\
\
├── Read Employees\
├── Clean Data\
├── Validate Records\
├── Write Delta Table\
└── Send Email

Here:

- **Job** = Entire pipeline

- **Tasks** = Individual processing steps

A Job can contain:

- One task

- Ten tasks

- Hundreds of tasks

Tasks can run:

- Sequentially

- In parallel

- Based on dependencies

**YouTube**

- **Databricks Workflow Jobs and Tasks**\
  https://www.youtube.com/results?search_query=Databricks+Workflow+Jobs+Tasks

------------------------------------------------------------------------

# [README](./../../../README.md)
