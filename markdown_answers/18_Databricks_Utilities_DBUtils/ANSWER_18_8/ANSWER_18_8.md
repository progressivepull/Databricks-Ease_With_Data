# ANSWER 18 8

**Question 8**

**What is the primary purpose of DBUtils Secrets?**

**A. To optimize Delta Lake performance** ❌ Incorrect

- Secrets have nothing to do with performance.

**B. To create notebook widgets** ❌ Incorrect

- Widgets are separate.

**C. To securely access sensitive information such as passwords and API keys** ✅ Correct

Instead of writing:

password = "MyPassword123"

Use:

password =\
dbutils.secrets.get(\
scope="prod",\
key="sql-password"\
)

Benefits:

- Password isn't visible.

- Stored securely.

- Easier administration.

Secrets commonly store:

- Passwords

- API Keys

- OAuth Tokens

- Connection Strings

- Certificates

**D. To schedule Databricks jobs** ❌ Incorrect

- Jobs are managed elsewhere.

**E. To manage Spark executors** ❌ Incorrect

- Executors are compute resources.

**Memory Trick**

Secrets

↓

Sensitive Information

# [README](./../../../README.md)
