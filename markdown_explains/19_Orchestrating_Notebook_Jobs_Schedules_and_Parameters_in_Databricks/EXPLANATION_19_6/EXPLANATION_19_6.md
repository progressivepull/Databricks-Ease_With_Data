# EXPLANATION 19 6

**Question 5**

**How does the child notebook generate the name of the Delta table it writes?**

**Correct Answer: C. It dynamically builds the table name using the department parameter (for example, dev.branch.dept_sales).**

**Explanation**

Instead of hardcoding table names, the notebook constructs them dynamically.

Example:

department = dbutils.widgets.get("department").lower()\
\
table_name = f"dev.branch.dept\_{department}"

If:

department = Sales

then:

table_name = dev.branch.dept_sales

If:

department = HR

then:

table_name = dev.branch.dept_hr

**Benefits**

- One notebook writes to many tables.

- Less duplicated code.

- Easier maintenance.

- More scalable.

**YouTube**

- **Delta Tables in Databricks**\
  https://www.youtube.com/results?search_query=Databricks+Delta+Table+tutorial

# [README](./../../../README.md)
