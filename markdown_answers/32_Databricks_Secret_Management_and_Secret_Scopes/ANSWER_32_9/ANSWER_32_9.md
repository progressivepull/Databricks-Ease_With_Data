# ANSWER 32 9

**Question 9**

**What is the primary purpose of Access Control Lists (ACLs) on Secret Scopes?**

**A. To improve Spark job performance ❌ Incorrect**

- ACLs affect **security**, not performance.

------------------------------------------------------------------------

**B. To automatically back up secrets to cloud storage ❌ Incorrect**

- ACLs do not perform backups.

------------------------------------------------------------------------

**C. To determine who can use, read, and manage Secret Scopes ✅ Correct**

ACLs define permissions such as:

- **READ** – retrieve secrets

- **WRITE** – add or update secrets

- **MANAGE** – administer the Secret Scope

Example:

Admins → READ, WRITE, MANAGE

Developers → READ

Analysts → No Access

------------------------------------------------------------------------

**D. To convert secrets into environment variables automatically ❌ Incorrect**

- Secret retrieval and environment variables are separate concepts.

**E. To synchronize secrets across multiple Databricks workspaces ❌ Incorrect**

- ACLs control permissions, not synchronization.

------------------------------------------------------------------------

**Why C is correct**

ACLs enforce the principle of least privilege by controlling who can access and manage secrets.

------------------------------------------------------------------------

# [README](./../../../README.md)
