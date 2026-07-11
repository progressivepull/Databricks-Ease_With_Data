# ANSWER 32 6

**Question 6**

**What happens when a secret is retrieved using dbutils.secrets.get() inside a Databricks notebook?**

**A. The secret is automatically written to a Delta table. ❌ Incorrect**

- Retrieving a secret does not store it anywhere.

------------------------------------------------------------------------

**B. The secret value is displayed in plain text. ❌ Incorrect**

- Databricks protects secrets from being displayed directly.

------------------------------------------------------------------------

**C. Databricks automatically redacts the secret value in notebook output. ✅ Correct**

Example:

password = dbutils.secrets.get(...)

print(password)

Instead of showing:

MySecretPassword123

The notebook displays something like:

\[REDACTED\]

This reduces the risk of exposing credentials during demonstrations or code reviews.

------------------------------------------------------------------------

**D. The secret is copied into Unity Catalog metadata. ❌ Incorrect**

- Unity Catalog does not store retrieved secrets.

**E. The secret is permanently cached in the notebook source code. ❌ Incorrect**

- Secret values are not written back into the notebook source.

------------------------------------------------------------------------

**Why C is correct**

Databricks automatically redacts secret values in notebook output to help prevent accidental disclosure.

------------------------------------------------------------------------

# [README](./../../../README.md)
