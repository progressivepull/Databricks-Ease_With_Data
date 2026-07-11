# ANSWER 32 10

**Question 10**

**Which statement correctly compares Azure Key Vault-backed and Databricks-backed Secret Scopes?**

**A. Both store secrets only inside Unity Catalog. ❌ Incorrect**

- Unity Catalog manages metadata and governance.

- It is not where Secret Scope values are stored.

------------------------------------------------------------------------

**B. Azure Key Vault-backed scopes store secrets in Azure Key Vault, while Databricks-backed scopes store secrets inside Databricks. ✅ Correct**

Comparison:

| **Azure Key Vault-backed** | **Databricks-backed** |
|----|----|
| Secrets stored in Azure Key Vault | Secrets stored in Databricks |
| Centralized with Azure services | Managed within Databricks |
| Uses Key Vault for storage | Uses Databricks-managed encrypted storage |

Both types can be accessed in notebooks with:

dbutils.secrets.get(scope="...", key="...")

The retrieval method is the same—the storage location differs.

------------------------------------------------------------------------

**C. Databricks-backed scopes require Azure Key Vault to function. ❌ Incorrect**

- Databricks-backed scopes work independently of Azure Key Vault.

------------------------------------------------------------------------

**D. Azure Key Vault-backed scopes can only store database passwords. ❌ Incorrect**

- They can store many types of secrets, including:

  - API keys

  - OAuth tokens

  - SAS tokens

  - Connection strings

  - Certificates

  - Database credentials

------------------------------------------------------------------------

**E. Neither type supports retrieving secrets using dbutils.secrets.get(). ❌ Incorrect**

- Both Secret Scope types use the same retrieval method:

dbutils.secrets.get(scope="...", key="...")

The difference is **where the secret is stored**, not how it is retrieved.

------------------------------------------------------------------------

**Why B is correct**

The key distinction is the **storage location**:

- **Azure Key Vault-backed Secret Scopes** keep the secret values in **Azure Key Vault**, with Databricks securely retrieving them when requested.

- **Databricks-backed Secret Scopes** store the secret values in **Databricks-managed encrypted storage**.

From a notebook, both are accessed using the same dbutils.secrets.get() API, providing a consistent developer experience while allowing organizations to choose the storage mechanism that best fits their security and governance requirements.

# [README](./../../../README.md)
