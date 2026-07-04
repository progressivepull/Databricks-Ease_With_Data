# EXPLANATION 19 5

**Question 4**

**Which two conditions are used by the child notebook to filter employee data?**

**Correct Answer: C. Department parameter and Active Record = 1**

**Explanation**

The notebook filters employees using two criteria:

1.  The department passed by the parent notebook.

2.  Only active employee records (Active Record = 1).

Example:

department = dbutils.widgets.get("department")\
\
filtered_df = (\
employee_df\
.filter(employee_df.Department == department)\
.filter(employee_df.Active_Record == 1)\
)

If the parent passes:

Finance

the child notebook processes only active Finance employees.

This prevents inactive or historical records from being included.

**Why is this important?**

Many enterprise systems keep historical employee records. Filtering on Active Record = 1 ensures only current records are processed.

**YouTube**

- **PySpark DataFrame Filter Tutorial**\
  https://www.youtube.com/results?search_query=PySpark+DataFrame+filter+Databricks

# [README](./../../../README.md)
