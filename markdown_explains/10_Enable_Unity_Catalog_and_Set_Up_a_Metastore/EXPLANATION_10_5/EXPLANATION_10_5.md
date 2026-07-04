# EXPLANATION 10 5

**Question 5**

**What is the primary purpose of the Azure Databricks Access Connector?**

**Correct Answer:**\
✅ **To securely authenticate Databricks to Azure Storage using a Managed Identity**

**Explanation**

The **Azure Databricks Access Connector** provides a **Managed Identity** that Unity Catalog uses to securely access Azure Storage.

Instead of storing:

- Passwords

- Storage Keys

- Connection Strings

Databricks authenticates using Azure's Managed Identity service.

Workflow:

Databricks\
\
↓\
\
Access Connector\
\
↓\
\
Managed Identity\
\
↓\
\
Azure Storage

This approach improves security because no secrets need to be embedded in notebooks or configuration files.

**YouTube**

**Azure Databricks Access Connector**

https://www.youtube.com/results?search_query=Azure+Databricks+Access+Connector

# [README](./../../../README.md)
