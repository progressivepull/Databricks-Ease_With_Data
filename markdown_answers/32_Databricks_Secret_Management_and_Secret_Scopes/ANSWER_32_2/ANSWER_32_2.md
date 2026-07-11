# ANSWER 32 2

**Question 2**

**Which two types of Secret Scopes are supported by Databricks?**

**A. Local Secret Scopes and Global Secret Scopes ❌ Incorrect**

- These are **not** Databricks Secret Scope types.

------------------------------------------------------------------------

**B. Azure Key Vault-backed and Databricks-backed Secret Scopes ✅ Correct**

Databricks supports two types:

**Databricks-backed**

Secrets are stored inside Databricks.

Notebook

↓

Databricks Secret Scope

↓

Stored in Databricks

**Azure Key Vault-backed**

Secrets remain in Azure Key Vault.

Notebook

↓

Secret Scope

↓

Azure Key Vault

Databricks retrieves them when needed.

------------------------------------------------------------------------

**C. AWS Secrets Manager-backed and Google Secret Manager-backed Secret Scopes only ❌ Incorrect**

- Databricks integrates with various cloud services, but the supported Secret Scope types in Azure Databricks are **Databricks-backed** and **Azure Key Vault-backed**.

------------------------------------------------------------------------

**D. Workspace-backed and Cluster-backed Secret Scopes ❌ Incorrect**

- These are not valid Secret Scope types.

------------------------------------------------------------------------

**E. SQL-backed and Delta-backed Secret Scopes ❌ Incorrect**

- Secret Scopes are unrelated to SQL databases or Delta tables.

------------------------------------------------------------------------

**Why B is correct**

The two supported Secret Scope implementations are:

- Databricks-backed

- Azure Key Vault-backed

------------------------------------------------------------------------

# [README](./../../../README.md)
