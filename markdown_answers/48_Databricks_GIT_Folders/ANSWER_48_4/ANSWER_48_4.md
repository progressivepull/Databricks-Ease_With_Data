# ANSWER 48 4

**Question 4**

**How does Databricks authenticate with Azure DevOps when connecting a Git repository?**

**A. Azure Active Directory only** ❌ Incorrect

- Azure AD authenticates users, but the lesson specifically demonstrates using a PAT.

**B. Username and Personal Access Token (PAT)** ✅ Correct

- Databricks typically connects using:

  - Azure DevOps username

  - Personal Access Token (PAT)

The PAT acts like a secure password for Git operations.

Example

Username

john@company.com

PAT

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

**C. SSH private key only** ❌ Incorrect

- SSH authentication exists in Git generally, but the lesson uses PAT authentication.

**D. Databricks Access Token only** ❌ Incorrect

- Databricks access tokens authenticate to Databricks APIs, not Azure DevOps Git repositories.

**E. Unity Catalog credentials** ❌ Incorrect

- Unity Catalog credentials are unrelated to Git authentication.

**Key Concept**

**Azure DevOps Git authentication = Username + PAT (per the lesson).**

# [README](./../../../README.md)
