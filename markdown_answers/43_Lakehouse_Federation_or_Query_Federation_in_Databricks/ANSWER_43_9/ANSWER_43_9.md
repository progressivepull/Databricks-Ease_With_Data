# ANSWER 43 9

**Question 9**

**Which feature allows Lakehouse Federation credentials to be stored securely instead of hardcoding usernames and passwords in SQL scripts?**

**A. Delta Transaction Log** ❌ Incorrect

- Transaction logs track table changes.

- They do not store credentials.

**B. Databricks Secret Scopes or Azure Key Vault-backed Secret Scopes** ✅ Correct

- Secret Scopes securely store:

  - Usernames

  - Passwords

  - Tokens

  - Connection strings

- SQL scripts can reference secrets instead of exposing credentials.

Example:

Instead of:

Password = MyPassword123

Use:

Password = secret(scope, key)

**C. SQL Warehouse Cache** ❌ Incorrect

- Cache stores query data, not secrets.

**D. Unity Catalog Volumes** ❌ Incorrect

- Volumes store files.

**E. Materialized Views** ❌ Incorrect

- Materialized Views store query results.

**Key Concept**

**Never hardcode credentials—use Secret Scopes or Azure Key Vault-backed Secret Scopes.**

# [README](./../../../README.md)
