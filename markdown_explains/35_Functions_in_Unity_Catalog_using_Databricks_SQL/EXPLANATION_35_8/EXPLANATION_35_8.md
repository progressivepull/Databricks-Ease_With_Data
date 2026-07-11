# EXPLANATION 35 8

**Question 8**

**How is a table function called in Databricks SQL?**

**Correct Answer:** **C. SELECT \* FROM function_name(...)**

**Explanation**

A table function returns an entire table, so it is referenced in the FROM clause.

Example:

SELECT \*

FROM my_table_function(100);

**Why the Correct Answer is Correct**

Because the function returns multiple rows, SQL treats it as a table source rather than a single value.

**Why the Other Answers Are Wrong**

The incorrect options use syntax appropriate for scalar functions.

**YouTube Video**\
https://www.youtube.com/watch?v=goOtM0Qf0qE

**Direct YouTube Link**\
https://www.youtube.com/watch?v=goOtM0Qf0qE

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+table+functions

------------------------------------------------------------------------

# [README](./../../../README.md)
