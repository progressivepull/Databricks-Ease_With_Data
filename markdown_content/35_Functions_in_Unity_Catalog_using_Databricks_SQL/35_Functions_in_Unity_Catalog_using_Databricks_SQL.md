# 35 Functions in Unity Catalog using Databricks SQL

**Functions in Unity Catalog using Databricks SQL**

This lesson explains how **Functions** work in **Unity Catalog** and Databricks SQL. It covers built-in SQL functions, User-Defined Functions (UDFs), scalar functions, table functions, SQL and Python UDFs, and how to register reusable functions in Unity Catalog so they can be shared across SQL and PySpark workloads.

------------------------------------------------------------------------

**1. Functions in Unity Catalog**

Functions are securable objects stored inside Unity Catalog.

Hierarchy:

Metastore\
│\
Catalog\
│\
Schema\
│\
Functions

Because functions are Unity Catalog objects, they can be:

- Shared

- Secured

- Managed

- Granted permissions

just like tables and views.

------------------------------------------------------------------------

**2. Types of Functions**

Databricks supports two major categories.

**Built-in Functions**

Provided automatically by Databricks.

Examples include:

- LOWER()

- UPPER()

- CONCAT()

- CURRENT_USER()

- EXPR()

No registration is required.

------------------------------------------------------------------------

**User-Defined Functions (UDFs)**

Created by developers.

Advantages:

- Encapsulate business logic

- Reusable

- Registered in Unity Catalog

- Can be shared across users

------------------------------------------------------------------------

**3. Unity Catalog UDF vs PySpark Session UDF**

There is an important distinction.

**PySpark Session UDF**

- Exists only during the current Spark session

- Not shared

- Disappears when the session ends

------------------------------------------------------------------------

**Unity Catalog Function**

- Registered permanently

- Shared across users

- Available in SQL

- Can be called from PySpark

- Governed by Unity Catalog permissions

------------------------------------------------------------------------

**4. Scalar vs Table Functions**

Unity Catalog supports two types of UDFs.

**Scalar Function**

Input:

Salary

Output:

3000

One output value.

------------------------------------------------------------------------

**Table Function**

Input:

Department

Output:

Employee Table

Multiple rows returned.

------------------------------------------------------------------------

**5. Scalar Function**

A scalar function always returns **one value**.

Example:

Salary\
\
↓\
\
Tax\
\
↓\
\
3000

Return types may include:

- Integer

- Double

- String

- Boolean

- Date

Any single value qualifies as a scalar function.

------------------------------------------------------------------------

**6. Creating a SQL Scalar Function**

Example syntax:

CREATE OR REPLACE FUNCTION

The lesson creates:

dev.bronze.tax_sql

Function logic:

Tax = Salary × 30%

Characteristics:

- Input: Salary

- Output: Tax

- Language: SQL

------------------------------------------------------------------------

**7. CREATE OR REPLACE**

Using:

CREATE OR REPLACE FUNCTION

allows updating a function without manually dropping it first.

Without REPLACE:

- Drop function

- Recreate function

With REPLACE:

- Simply rerun the statement

------------------------------------------------------------------------

**8. Three-Level Namespace**

Functions are registered using Unity Catalog's namespace.

Catalog.Schema.Function

Example:

dev.bronze.tax_sql

This makes functions globally available within the catalog.

------------------------------------------------------------------------

**9. Calling a Scalar Function**

Example:

SELECT dev.bronze.tax_sql(10000);

Output:

3000

The scalar function returns one calculated value.

------------------------------------------------------------------------

**10. Using Scalar Functions in Queries**

Functions can be used inside SQL statements.

Example:

Employee Salary\
\
↓\
\
Tax Function\
\
↓\
\
Tax Column

Result:

Employee\
Salary\
Tax

This enables reusable business calculations across many queries.

------------------------------------------------------------------------

**11. Calling Unity Catalog Functions from PySpark**

Unity Catalog SQL functions can also be used in PySpark.

Unlike SQL:

They must be wrapped using:

expr()

Example:

expr("dev.bronze.tax_sql(salary)")

This allows PySpark DataFrames to call registered SQL functions.

------------------------------------------------------------------------

**12. Python Functions**

Unity Catalog also supports Python UDFs.

Example:

Fruit Name\
\
↓\
\
Python API Call\
\
↓\
\
Nutrition Information

The lesson creates a Python function that:

- Accepts a fruit name

- Calls an external API

- Returns nutritional information

------------------------------------------------------------------------

**13. Python Function Syntax**

Python UDFs specify:

LANGUAGE PYTHON

The Python implementation is enclosed within:

\$\$\
Python Code\
\$\$

This separates the SQL definition from the embedded Python code.

------------------------------------------------------------------------

**14. Python UDF Example**

Workflow:

Banana\
\
↓\
\
Python Function\
\
↓\
\
REST API\
\
↓\
\
JSON\
\
↓\
\
String Output

Although the function calls an external API, it still behaves as a scalar function because it returns a single string value.

------------------------------------------------------------------------

**15. Table Functions**

A table function returns multiple rows instead of a single value.

Example:

Input:

Department = D101

Output:

Employee ID\
Employee Name

Multiple rows are returned for employees in that department.

------------------------------------------------------------------------

**16. Creating a Table Function**

The lesson creates:

dev.bronze.get_emp

Input:

Department Code

Returns:

Employee ID\
Employee Name

The function internally queries the Employee table and returns matching rows.

------------------------------------------------------------------------

**17. Calling Table Functions**

Unlike scalar functions, table functions must be queried using:

SELECT \*\
FROM function(...)

Example:

SELECT \*\
FROM dev.bronze.get_emp('D101');

Attempting to call a table function like a scalar function results in an error because it returns a result set rather than a single value.

------------------------------------------------------------------------

**18. Function Metadata**

Catalog Explorer displays details for each function.

Information includes:

- Input parameters

- Return type

- Function type (Scalar or Table)

- Language (SQL or Python)

- Definition

This makes it easy to inspect and understand registered functions.

------------------------------------------------------------------------

**19. Function Permissions**

Functions have their own permission model.

Administrators can control:

- Who can execute a function

- Who can manage the function

- Who can view the definition

Because functions are Unity Catalog objects, they follow the same governance model as tables and views.

**20. Function Parameters**

Functions may have:

- Zero parameters

- One parameter

- Multiple parameters

The number of inputs does **not** determine the function type.

The determining factor is the output:

- One value → Scalar Function

- Multiple rows → Table Function

------------------------------------------------------------------------

**Scalar vs Table Functions**

| **Feature** | **Scalar Function** | **Table Function**             |
|-------------|---------------------|--------------------------------|
| Output      | One value           | Multiple rows                  |
| Return Type | Single data type    | Table                          |
| SQL Usage   | SELECT function()   | SELECT \* FROM function()      |
| Example     | Calculate tax       | Return employees by department |

------------------------------------------------------------------------

**SQL vs Python UDFs**

| **Feature**                 | **SQL UDF**        | **Python UDF** |
|-----------------------------|--------------------|----------------|
| Language                    | SQL                | Python         |
| Business Logic              | SQL expressions    | Python code    |
| External APIs               | No                 | Yes            |
| Registered in Unity Catalog | Yes                | Yes            |
| Callable from SQL           | Yes                | Yes            |
| Callable from PySpark       | Yes (using expr()) | Yes            |

------------------------------------------------------------------------

**Best Practices**

- Use **built-in functions** whenever possible because they are optimized and require no maintenance.

- Register commonly used business logic as **Unity Catalog UDFs** so it can be reused across notebooks, SQL queries, jobs, and users.

- Use **scalar functions** when a calculation returns a single value, and **table functions** when the result is a set of rows.

- Use **CREATE OR REPLACE FUNCTION** during development to simplify updates without dropping existing functions.

- When calling Unity Catalog SQL functions from **PySpark**, wrap them with **expr()**.

- Secure functions with Unity Catalog permissions just as you would tables and views to ensure proper governance and controlled access.

# [README](./../../../README.md)
