# EXPLANATION 35 4

**Question 4**

**What distinguishes a scalar function from a table function?**

**Correct Answer:** **B. Scalar functions return one value, while table functions return multiple rows.**

**Explanation**

**Scalar Function**

SELECT LOWER('ABC');

Returns:

abc

**Table Function**

SELECT \*

FROM my_table_function(...);

Returns an entire result set consisting of multiple rows and columns.

**Why the Correct Answer is Correct**

The distinction is based on the **type of output**:

- Scalar → one value.

- Table → many rows.

**Why the Other Answers Are Wrong**

They confuse implementation language with the function's return type.

**YouTube Video**\
https://www.youtube.com/watch?v=goOtM0Qf0qE

**Direct YouTube Link**\
https://www.youtube.com/watch?v=goOtM0Qf0qE

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+scalar+function+vs+table+function

------------------------------------------------------------------------

# [README](./../../../README.md)
