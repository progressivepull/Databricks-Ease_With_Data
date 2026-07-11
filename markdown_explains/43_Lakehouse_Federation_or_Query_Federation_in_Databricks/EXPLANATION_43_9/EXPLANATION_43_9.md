# EXPLANATION 43 9

**Question 9**

**Which feature allows Lakehouse Federation credentials to be stored securely instead of hardcoding usernames and passwords in SQL scripts?**

**Correct Answer:**\
**B. Databricks Secret Scopes or Azure Key Vault-backed Secret Scopes**

**Why B is Correct**

Instead of embedding credentials in SQL:

password='mypassword'

Databricks recommends using:

- Databricks Secret Scopes

- Azure Key Vault-backed Secret Scopes (on Azure)

Benefits include:

- encrypted credential storage

- centralized secret management

- improved security

- easier credential rotation

**Why the other choices are wrong**

Credentials should not be hardcoded in notebooks or SQL scripts.

**Memory Tip**

**Secrets, not passwords.**

**Individual YouTube Video**

https://www.youtube.com/watch?v=JQh7kW8M4iM

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Secret+Scopes

------------------------------------------------------------------------

# [README](./../../../README.md)
