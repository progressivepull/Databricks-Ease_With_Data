# EXPLANATION 22 8

**Question 7**

**What is the difference between Task Parameters and Job Parameters?**

**Correct Answer: B. Job Parameters are automatically available to every task, while Task Parameters apply only to individual tasks.**

**Explanation**

**Job Parameters**

Defined once and shared with every task.

Example:

Environment = DEV\
RunDate = 2026-07-02

All tasks can access these values.

------------------------------------------------------------------------

**Task Parameters**

Only available to one specific task.

Example:

Notebook Task\
\
department = Sales

Another notebook might receive:

department = Finance

**Analogy**

Think of a company project:

- Job Parameters = Company-wide instructions.

- Task Parameters = Instructions specific to one employee.

**YouTube**

- **Databricks Workflow Parameters**\
  https://www.youtube.com/results?search_query=Databricks+Workflow+Parameters

------------------------------------------------------------------------

# [README](./../../../README.md)
