# EXPLANATION 19 8

**Question 7**

**Which DBUtils command is used by the parent notebook to execute the child notebook?**

**Correct Answer: B. dbutils.notebook.run()**

**Explanation**

The parent notebook launches another notebook using:

dbutils.notebook.run(\
"/Shared/Employee_Load",\
timeout_seconds=300,\
arguments={"department": "Sales"}\
)

The command:

- Starts the child notebook.

- Waits until it completes.

- Returns the value from dbutils.notebook.exit().

This is one of the most common notebook orchestration techniques in Databricks.

**YouTube**

- **Databricks Notebook Run Tutorial**\
  https://www.youtube.com/results?search_query=dbutils.notebook.run+tutorial

# [README](./../../../README.md)
