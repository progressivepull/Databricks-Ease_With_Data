# ANSWER 32 3

**Question 3**

**In an Azure Key Vault-backed Secret Scope, where are the actual secret values stored?**

**A. Inside every Databricks notebook ❌ Incorrect**

- Storing secrets in notebooks defeats the purpose of Secret Scopes.

------------------------------------------------------------------------

**B. In Unity Catalog ❌ Incorrect**

- Unity Catalog manages metadata and governance.

- It does not store Secret Scope values.

------------------------------------------------------------------------

**C. Inside Azure Key Vault ✅ Correct**

The actual secrets stay inside Azure Key Vault.

Workflow:

Notebook

↓

Secret Scope

↓

Azure Key Vault

Databricks requests the secret when needed.

------------------------------------------------------------------------

**D. In Delta Lake tables ❌ Incorrect**

- Delta tables store business data, not credentials.

**E. On the Spark driver node ❌ Incorrect**

- Secrets may be used by the driver during execution but are not permanently stored there.

------------------------------------------------------------------------

**Why C is correct**

With a Key Vault-backed scope, Databricks acts as a secure bridge to Azure Key Vault, where the secrets remain stored.

------------------------------------------------------------------------

# [README](./../../../README.md)
