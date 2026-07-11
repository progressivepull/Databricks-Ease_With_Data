# ANSWER 39 9

**Question 9**

**What authentication mechanism is typically used for Open Sharing?**

**A. Workspace Sharing Identifier ❌ Incorrect**

Sharing Identifiers are used for Databricks-to-Databricks sharing.

**B. Kerberos tickets ❌ Incorrect**

Kerberos is unrelated.

**C. OAuth user credentials only ❌ Incorrect**

OAuth alone is not the standard authentication mechanism for Open Sharing.

**D. Sharing tokens ✅ Correct**

Open Sharing typically uses secure sharing tokens.

Example:

Provider

│

Creates Token

│

Recipient

│

Uses Token

│

Reads Shared Data

Tokens securely authenticate external recipients.

**E. SSH keys ❌ Incorrect**

SSH is unrelated.

**Why D is correct**

Sharing tokens securely authenticate recipients accessing Open Sharing endpoints.

# [README](./../../../README.md)
