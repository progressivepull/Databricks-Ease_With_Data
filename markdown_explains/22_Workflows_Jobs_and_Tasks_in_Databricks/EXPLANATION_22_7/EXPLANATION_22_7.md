# EXPLANATION 22 7

**Question 6**

**How are notebook parameters typically created so that Workflow parameters can populate them?**

**Correct Answer: C. Using dbutils.widgets**

**Explanation**

Workflow parameters are passed into notebook widgets.

Create the widget:

dbutils.widgets.text(\
"department",\
"Sales"\
)

Retrieve its value:

department = dbutils.widgets.get("department")

When the workflow starts, it automatically populates the widget with the configured value.

This allows the same notebook to run for different departments, dates, or environments without changing the code.

**YouTube**

- **Databricks Widgets Tutorial**\
  https://www.youtube.com/results?search_query=Databricks+Widgets+Tutorial

------------------------------------------------------------------------

# [README](./../../../README.md)
