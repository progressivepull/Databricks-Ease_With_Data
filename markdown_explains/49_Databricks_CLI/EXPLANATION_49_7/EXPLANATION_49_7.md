# EXPLANATION 49 7

**Question 7**

**Where are Databricks CLI authentication profiles stored?**

**Correct Answer:**\
**C. .databricks.cfg**

**Why C is Correct**

The Databricks CLI stores authentication profiles in:

~/.databricks.cfg

(on Windows, this file is located in the user's home directory, such as %USERPROFILE%\\databricks.cfg).

The file can contain multiple named profiles, making it easy to switch between development, test, and production workspaces. ([docs.databricks.com](https://docs.databricks.com/aws/en/dev-tools/auth/config-profiles))

**Why the other choices are wrong**

Authentication profiles are not stored in notebooks, Git repositories, or SQL Warehouses.

**Memory Tip**

**Credentials live in .databricks.cfg**

**Individual YouTube Video**

https://www.youtube.com/watch?v=5s8N4vV5m9M

**YouTube Search**

https://www.youtube.com/results?search_query=.databricks.cfg+Databricks+CLI

------------------------------------------------------------------------

# [README](./../../../README.md)
