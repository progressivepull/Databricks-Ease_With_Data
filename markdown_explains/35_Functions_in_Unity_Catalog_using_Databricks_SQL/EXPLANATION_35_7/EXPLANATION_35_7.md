# EXPLANATION 35 7

**Question 7**

**Which keyword is used when defining a Python User-Defined Function in Unity Catalog?**

**Correct Answer:** **C. LANGUAGE PYTHON**

**Explanation**

When creating a Python UDF in Unity Catalog, the SQL definition includes the clause:

CREATE FUNCTION catalog.schema.my_function(...)

RETURNS STRING

LANGUAGE PYTHON

AS \$\$

...

\$\$;

The LANGUAGE PYTHON clause tells Unity Catalog that the function implementation is written in Python.

**Why the Correct Answer is Correct**

It is the official SQL syntax for creating Python UDFs in Unity Catalog.

**Why the Other Answers Are Wrong**

The other keywords are not valid language declarations for Unity Catalog Python functions.

**YouTube Video**\
https://www.youtube.com/watch?v=goOtM0Qf0qE

**Direct YouTube Link**\
https://www.youtube.com/watch?v=goOtM0Qf0qE

**YouTube Search**\
https://www.youtube.com/results?search_query=Unity+Catalog+LANGUAGE+PYTHON+UDF

------------------------------------------------------------------------

# [README](./../../../README.md)
