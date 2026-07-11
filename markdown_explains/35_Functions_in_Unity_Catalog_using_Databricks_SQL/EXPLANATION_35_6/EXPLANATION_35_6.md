# EXPLANATION 35 6

**Question 6**

**How should a Unity Catalog SQL function be called from a PySpark DataFrame?**

**Correct Answer:** **B. By wrapping the function call with expr()**

**Explanation**

PySpark can invoke SQL functions using the expr() API.

Example:

from pyspark.sql.functions import expr

df.select(expr("catalog.schema.my_function(customer_name)"))

expr() allows SQL expressions, including Unity Catalog functions, to be embedded within DataFrame transformations.

**Why the Correct Answer is Correct**

expr() bridges the SQL function into the DataFrame API.

**Why the Other Answers Are Wrong**

They either reference nonexistent APIs or treat the SQL function like a native Python function.

**YouTube Video**\
https://www.youtube.com/watch?v=goOtM0Qf0qE

**Direct YouTube Link**\
https://www.youtube.com/watch?v=goOtM0Qf0qE

**YouTube Search**\
https://www.youtube.com/results?search_query=PySpark+expr+Unity+Catalog+function

------------------------------------------------------------------------

# [README](./../../../README.md)
