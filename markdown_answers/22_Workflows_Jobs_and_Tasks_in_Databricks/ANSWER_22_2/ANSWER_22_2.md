# ANSWER 22 2

**Question 2**

**In Databricks Workflows, what is the relationship between a Job and a Task?**

**A. A Task contains multiple Jobs.** ❌ Incorrect

- The relationship is reversed.

**B. A Job is a complete workflow composed of one or more Tasks.** ✅ Correct

Hierarchy:

Job\
├── Task 1\
├── Task 2\
├── Task 3\
└── Task 4

The Job is the container.

Each Task performs one piece of work.

Example:

Job\
\
↓\
\
Read CSV\
\
↓\
\
Clean Data\
\
↓\
\
MERGE\
\
↓\
\
Send Email

**C. Jobs and Tasks are identical concepts.** ❌ Incorrect

- A Job is much larger than an individual Task.

**D. A Task can only contain SQL code.** ❌ Incorrect

- Tasks can execute:

  - Notebooks

  - Python

  - SQL

  - DLT

  - JARs

  - dbt

  - and more.

**E. A Job can contain only one Task.** ❌ Incorrect

- Jobs may contain many tasks.

------------------------------------------------------------------------

**Memory Trick**

Job

↓

Many Tasks

------------------------------------------------------------------------

# [README](./../../../README.md)
