# EXPLANATION 18 10

**Question 9**

**Which DBUtils notebook command executes another notebook as part of a workflow?**

**Correct Answer: C. dbutils.notebook.run()**

**Explanation**

One notebook can call another.

Example

result =\
dbutils.notebook.run(\
"/Shared/LoadSales",\
300,\
{"year":"2025"})

This means:

- run notebook

- wait up to 300 seconds

- pass parameters

- receive result

This is frequently used in:

- ETL pipelines

- workflows

- orchestration

- modular notebook design

------------------------------------------------------------------------

**Think of it like**

Python:

callFunction()

except the function is an entire notebook.

------------------------------------------------------------------------

**YouTube**

- <https://www.youtube.com/watch?v=zMUiDYgqlq0>

------------------------------------------------------------------------

# [README](./../../../README.md)
