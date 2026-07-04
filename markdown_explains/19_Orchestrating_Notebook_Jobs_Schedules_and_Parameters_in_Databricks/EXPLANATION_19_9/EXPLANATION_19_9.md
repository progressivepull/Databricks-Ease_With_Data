# EXPLANATION 19 9

**Question 8**

**How are parameters passed from the parent notebook to the child notebook?**

**Correct Answer: C. Using a Python dictionary passed to dbutils.notebook.run()**

**Explanation**

Parameters are passed as key-value pairs in a Python dictionary.

Example:

dbutils.notebook.run(\
"/Shared/Employee_Load",\
300,\
{\
"department": "Sales",\
"environment": "DEV"\
}\
)

Inside the child notebook:

department = dbutils.widgets.get("department")\
environment = dbutils.widgets.get("environment")

This allows a single notebook to handle many different scenarios.

**YouTube**

- **Passing Parameters Between Databricks Notebooks**\
  https://www.youtube.com/results?search_query=Passing+parameters+between+Databricks+notebooks

# [README](./../../../README.md)
