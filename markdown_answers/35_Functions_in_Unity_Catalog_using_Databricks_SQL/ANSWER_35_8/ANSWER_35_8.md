# ANSWER 35 8

**Question 8**

**How is a table function called in Databricks SQL?**

**A. SELECT function_name() ❌ Incorrect**

That's used for scalar functions.

------------------------------------------------------------------------

**B. CALL function_name() ❌ Incorrect**

CALL executes stored procedures, not table functions.

------------------------------------------------------------------------

**C. SELECT \* FROM function_name(...) ✅ Correct**

Example:

SELECT \*

FROM employee_lookup(10);

The function behaves like a virtual table.

------------------------------------------------------------------------

**D. RUN function_name() ❌ Incorrect**

No such SQL command.

------------------------------------------------------------------------

**E. EXECUTE function_name() ❌ Incorrect**

Not valid syntax for table functions.

------------------------------------------------------------------------

**Why C is correct**

Because a table function returns rows, SQL treats it like a table in the FROM clause.

------------------------------------------------------------------------

# [README](./../../../README.md)
