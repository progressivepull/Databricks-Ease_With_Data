# ANSWER 32 1

**Question 1**

**Why should sensitive information such as passwords and API keys be stored in Secret Scopes instead of hardcoded in notebooks?**

**A. Hardcoded credentials improve notebook performance. ❌ Incorrect**

- Credentials have **no meaningful impact on notebook performance**.

- Whether a password is hardcoded or retrieved from a Secret Scope, Spark performance is essentially unchanged.

- The real concern is **security**, not speed.

------------------------------------------------------------------------

**B. Secret Scopes automatically encrypt all Delta tables. ❌ Incorrect**

- Secret Scopes protect **credentials**, not data tables.

- Delta table encryption is handled by the cloud storage platform (Azure Storage, S3, GCS) and other security features.

- Secret Scopes do **not** encrypt your Delta Lake data.

------------------------------------------------------------------------

**C. Secret Scopes provide centralized, secure credential management and prevent accidental exposure. ✅ Correct**

This is exactly why Secret Scopes exist.

Benefits include:

- Centralized storage for secrets

- Avoid hardcoding passwords

- Easier credential rotation

- Fine-grained access control (ACLs)

- Automatic redaction in notebook output

Instead of:

password = "MySuperSecret123"

You use:

password = dbutils.secrets.get(

scope="prod",

key="db-password"

)

If the password changes, only the Secret Scope needs updating—not every notebook.

------------------------------------------------------------------------

**D. Hardcoded credentials are required for Databricks Jobs. ❌ Incorrect**

- Databricks Jobs can use Secret Scopes.

- In fact, using Secret Scopes is the recommended best practice.

------------------------------------------------------------------------

**E. Secret Scopes eliminate the need for authentication. ❌ Incorrect**

- Users still authenticate to Databricks.

- Secret Scopes securely store credentials but **do not replace authentication**.

------------------------------------------------------------------------

**Why C is correct**

Secret Scopes improve security by storing credentials in a centralized, protected location and reducing the risk of accidental exposure in notebooks or source control.

------------------------------------------------------------------------

# [README](./../../../README.md)
