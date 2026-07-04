# EXPLANATION 18 8

**Question 7**

**Which DBUtils command retrieves the current value of a widget?**

**Correct Answer: B. dbutils.widgets.get()**

**Explanation**

After creating a widget:

dbutils.widgets.text(\
"country",\
"USA"\
)

Retrieve its value:

country =\
dbutils.widgets.get("country")

If the user entered:

Canada

then

country = "Canada"

------------------------------------------------------------------------

**Why use this?**

Makes notebooks reusable.

Instead of changing code:

country="USA"

you read user input dynamically.

------------------------------------------------------------------------

**YouTube**

- <https://www.youtube.com/watch?v=zMUiDYgqlq0>

------------------------------------------------------------------------

# [README](./../../../README.md)
