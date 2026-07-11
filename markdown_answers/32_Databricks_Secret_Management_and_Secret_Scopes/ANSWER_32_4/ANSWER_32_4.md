# ANSWER 32 4

**Question 4**

**Which DBUtils command is used to retrieve the value of a secret?**

**A. dbutils.secrets.read() ❌ Incorrect**

- No such DBUtils method exists.

------------------------------------------------------------------------

**B. dbutils.secrets.fetch() ❌ Incorrect**

- Not a valid command.

------------------------------------------------------------------------

**C. dbutils.secrets.get() ✅ Correct**

Example:

password = dbutils.secrets.get(

scope="prod",

key="db-password"

)

This securely retrieves the secret.

------------------------------------------------------------------------

**D. dbutils.secrets.open() ❌ Incorrect**

- Not a DBUtils function.

------------------------------------------------------------------------

**E. dbutils.secrets.retrieve() ❌ Incorrect**

- Also not valid.

------------------------------------------------------------------------

**Why C is correct**

dbutils.secrets.get() is the standard API for retrieving secrets in Databricks notebooks.

------------------------------------------------------------------------

# [README](./../../../README.md)
