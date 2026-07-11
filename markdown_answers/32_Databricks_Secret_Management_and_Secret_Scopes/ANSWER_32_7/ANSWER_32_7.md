# ANSWER 32 7

**Question 7**

**How are Databricks-backed Secret Scopes typically created and managed?**

**A. Through Azure Portal only ❌ Incorrect**

- Azure Portal is used for Azure resources such as Key Vault.

- Databricks-backed scopes are not created there.

------------------------------------------------------------------------

**B. Using SQL commands in Databricks SQL Editor ❌ Incorrect**

- Secret Scope management is not done with SQL.

------------------------------------------------------------------------

**C. Using the Databricks CLI ✅ Correct**

Typical workflow:

databricks secrets create-scope

The Databricks CLI is commonly used to:

- create scopes

- manage secrets

- automate administration

------------------------------------------------------------------------

**D. Through Spark configuration files only ❌ Incorrect**

- Spark configuration does not create Secret Scopes.

------------------------------------------------------------------------

**E. Using Unity Catalog Explorer only ❌ Incorrect**

- Unity Catalog Explorer is not used to manage Databricks-backed Secret Scopes.

------------------------------------------------------------------------

**Why C is correct**

The Databricks CLI provides the standard administrative interface for creating and managing Databricks-backed Secret Scopes.

------------------------------------------------------------------------

# [README](./../../../README.md)
