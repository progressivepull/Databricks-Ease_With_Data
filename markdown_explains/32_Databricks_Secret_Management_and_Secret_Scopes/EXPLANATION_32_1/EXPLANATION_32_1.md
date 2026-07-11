# EXPLANATION 32 1

**Question 1**

**Why should sensitive information such as passwords and API keys be stored in Secret Scopes instead of hardcoded in notebooks?**

**Correct Answer:** **C. Secret Scopes provide centralized, secure credential management and prevent accidental exposure.**

**Explanation**

Hardcoding passwords, API keys, or tokens directly in notebooks is a security risk because anyone with notebook access can view the credentials. Databricks Secret Scopes provide a secure way to store sensitive information separately from code. Applications retrieve the secrets at runtime, making notebooks safer and easier to maintain.

**Why the Correct Answer is Correct**

Secret Scopes:

- Securely store credentials outside notebook code.

- Centralize credential management.

- Allow credentials to be updated without modifying notebooks.

- Reduce the risk of accidentally exposing secrets in source control or notebook output.

**Why the Other Answers Are Wrong**

- They imply credentials should be stored directly in notebooks or configuration files.

- They do not provide centralized security or access control.

- They increase the risk of credential leakage.

**YouTube Video**

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=f4SrT3DDdBo>

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+Secret+Scopes+tutorial

------------------------------------------------------------------------

# [README](./../../../README.md)
