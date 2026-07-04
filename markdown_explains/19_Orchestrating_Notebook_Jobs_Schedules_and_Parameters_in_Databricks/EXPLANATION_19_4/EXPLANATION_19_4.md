# EXPLANATION 19 4

**Question 3**

**Which DBUtils command retrieves the value entered into a widget?**

**Correct Answer: B. dbutils.widgets.get()**

**Explanation**

Creating a widget only displays the input box. To use the value, retrieve it with:

department = dbutils.widgets.get("department")

If the widget contains:

HR

then:

department

equals:

HR

The value can then be used in SQL or DataFrame operations.

Example:

df.filter(df.department == department)

**Why is this useful?**

The same notebook can process different departments simply by changing the widget value.

**YouTube**

- **Databricks Widgets and Parameters**\
  https://www.youtube.com/results?search_query=Databricks+widgets+parameters

# [README](./../../../README.md)
