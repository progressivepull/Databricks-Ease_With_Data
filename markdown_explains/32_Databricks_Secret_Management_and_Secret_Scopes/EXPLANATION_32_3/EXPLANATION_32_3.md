# EXPLANATION 32 3

**Question 3**

**In an Azure Key Vault-backed Secret Scope, where are the actual secret values stored?**

**Correct Answer:** **C. Inside Azure Key Vault**

**Explanation**

A Key Vault-backed Secret Scope does **not** copy secrets into Databricks. The secret values remain in Azure Key Vault, and Databricks retrieves them securely when requested.

**Why the Correct Answer is Correct**

Azure Key Vault is the system of record for the secret values.

**Why the Other Answers Are Wrong**

- Secrets are not stored in notebooks.

- They are not stored in Spark clusters.

- They are not duplicated into Databricks storage.

**YouTube Video**

[YouTube video link](https://www.youtube.com/watch?v=XbJ9ooxUtFA)

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=XbJ9ooxUtFA>

**YouTube Search**\
https://www.youtube.com/results?search_query=Azure+Key+Vault+Databricks+Secret+Scope

------------------------------------------------------------------------

# [README](./../../../README.md)
