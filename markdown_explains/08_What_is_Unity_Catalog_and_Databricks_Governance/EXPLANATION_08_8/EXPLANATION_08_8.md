# EXPLANATION 08 8

**Question 8**

**Which of the following is an example of a non-data securable object managed by Unity Catalog?**

**Correct Answer:**\
✅ **Storage Credential**

**Explanation**

A **Storage Credential** contains authentication information for accessing cloud storage.

Examples:

- Azure Managed Identity

- AWS IAM Role

- Google Cloud Service Account

It does **not** contain customer data.

Instead, it tells Unity Catalog **how to securely authenticate**.

Example:

Unity Catalog\
\
↓\
\
Storage Credential\
\
↓\
\
Azure Managed Identity\
\
↓\
\
ADLS Gen2

Storage Credentials are governance objects rather than data objects.

**YouTube**

**Storage Credentials & External Locations**

https://www.youtube.com/results?search_query=Unity+Catalog+Storage+Credential

# [README](./../../../README.md)
