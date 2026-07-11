# EXPLANATION 32 4

**Question 4**

**Which DBUtils command is used to retrieve the value of a secret?**

**Correct Answer:** **C. dbutils.secrets.get()**

**Explanation**

The dbutils.secrets.get() command retrieves a secret by specifying its scope and key.

Example:

password = dbutils.secrets.get(

scope="jdbc",

key="password"

)

Databricks automatically redacts the value if it appears in notebook output.

**Why the Correct Answer is Correct**

It is the official DBUtils method for retrieving secret values.

**Why the Other Answers Are Wrong**

The other commands either list scopes or perform unrelated DBUtils operations.

**YouTube Video**

[YouTube video link](https://www.youtube.com/watch?v=f4SrT3DDdBo)

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=f4SrT3DDdBo>

**YouTube Search**\
https://www.youtube.com/results?search_query=dbutils.secrets.get+Databricks

------------------------------------------------------------------------

# [README](./../../../README.md)
