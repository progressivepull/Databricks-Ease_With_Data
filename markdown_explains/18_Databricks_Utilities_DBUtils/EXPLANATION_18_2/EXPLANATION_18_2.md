# EXPLANATION 18 2

**Question 1**

**Which notebook languages support DBUtils?**

**Correct Answer: B. Python, Scala, and R**

**Explanation**

DBUtils is built directly into Databricks notebooks for:

- ✅ Python

- ✅ Scala

- ✅ R

It is **not available directly inside SQL notebooks** because SQL uses SQL syntax rather than programming language APIs. SQL notebooks have their own commands and widgets.

Example:

dbutils.fs.ls("/")

works in Python.

dbutils.fs.ls("/")

works in Scala.

dbutils.fs.ls("/")

works in R.

------------------------------------------------------------------------

**Why this matters**

Almost every Databricks data engineer uses DBUtils for:

- reading files

- copying files

- widgets

- secrets

- notebook workflows

------------------------------------------------------------------------

**YouTube**

- **18 DBUTILS Command \| Databricks Utilities \| Create Widgets in Databricks Notebooks**\
  <https://www.youtube.com/watch?v=zMUiDYgqlq0>

<!-- -->

- **Databricks Utilities Deep Dive \| Complete Guide**\
  [https://www.youtube.com/watch?v=79y6r_ndYko](https://www.youtube.com/watch?v=79y6r_ndYko&utm_source=chatgpt.com)

------------------------------------------------------------------------

# [README](./../../../README.md)
