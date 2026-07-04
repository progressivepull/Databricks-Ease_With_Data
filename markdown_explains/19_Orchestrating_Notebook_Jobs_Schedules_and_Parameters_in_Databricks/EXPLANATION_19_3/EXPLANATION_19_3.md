# EXPLANATION 19 3

**Question 2**

**Which DBUtils command is used to create a notebook parameter (widget)?**

**Correct Answer: C. dbutils.widgets.text()**

**Explanation**

Widgets create input fields at the top of a notebook.

Example:

dbutils.widgets.text(\
"department",\
"Sales"\
)

The notebook displays:

Department:\
\[ Sales \]

The user can type:

Finance

without changing the notebook code.

Other widget types include:

- text()

- dropdown()

- combobox()

- multiselect()

Widgets allow notebooks to become reusable templates.

**YouTube**

- **Databricks Widgets Tutorial**\
  https://www.youtube.com/results?search_query=Databricks+Widgets+Tutorial

# [README](./../../../README.md)
