# EXPLANATION 18 7

**Question 6**

**What is the primary purpose of DBUtils Widgets?**

**Correct Answer: C. To allow notebooks to accept runtime input parameters**

**Explanation**

Widgets create interactive input controls at the top of a notebook.

Examples:

- text box

- dropdown

- combobox

- multiselect

Example

dbutils.widgets.text(\
"name",\
"John"\
)

User sees

Name:\
\[ John \]

------------------------------------------------------------------------

Why?

Instead of editing code:

country="USA"

the user simply types:

Canada

The notebook runs using the new value.

Widgets are commonly used for:

- parameters

- dashboards

- scheduled jobs

- reusable notebooks

------------------------------------------------------------------------

**YouTube**

- <https://www.youtube.com/watch?v=zMUiDYgqlq0>

------------------------------------------------------------------------

# [README](./../../../README.md)
