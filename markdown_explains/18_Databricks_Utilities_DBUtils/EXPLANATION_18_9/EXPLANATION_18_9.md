# EXPLANATION 18 9

**Question 8**

**What is the primary purpose of DBUtils Secrets?**

**Correct Answer: C. To securely access sensitive information such as passwords and API keys**

**Explanation**

Never hardcode credentials like this:

password="MyPassword123"

Instead:

dbutils.secrets.get(\
scope="prod",\
key="db-password")

Databricks securely retrieves:

- passwords

- API keys

- tokens

- connection strings

- service principal secrets

The secret value is hidden from notebook output.

**Benefits**

- safer

- reusable

- centrally managed

- prevents accidental exposure

------------------------------------------------------------------------

**YouTube**

- <https://www.youtube.com/watch?v=zMUiDYgqlq0>

------------------------------------------------------------------------

# [README](./../../../README.md)
