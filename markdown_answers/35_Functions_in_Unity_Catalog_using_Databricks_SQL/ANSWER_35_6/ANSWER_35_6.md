# ANSWER 35 6

**Question 6**

**How should a Unity Catalog SQL function be called from a PySpark DataFrame?**

**A. By using spark.sqlFunction() directly ❌ Incorrect**

No such API exists.

------------------------------------------------------------------------

**B. By wrapping the function call with expr() ✅ Correct**

Example:

from pyspark.sql.functions import expr

df.select(

expr("sales.tax(price)")

)

expr() allows PySpark to execute SQL expressions, including Unity Catalog functions.

------------------------------------------------------------------------

**C. By importing the function into Python using import ❌ Incorrect**

SQL functions are not imported like Python modules.

------------------------------------------------------------------------

**D. By using spark.read.table() ❌ Incorrect**

That reads tables.

Not functions.

------------------------------------------------------------------------

**E. By converting it into a session UDF first ❌ Incorrect**

No conversion is needed.

------------------------------------------------------------------------

**Why B is correct**

expr() bridges SQL expressions into the PySpark DataFrame API.

------------------------------------------------------------------------

# [README](./../../../README.md)
