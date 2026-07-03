# ANSWER 10 5

**Question 5**

**What is the primary purpose of the Azure Databricks Access Connector?**

**A. To create Spark clusters automatically** ❌ Incorrect

- Cluster creation is unrelated to the Access Connector.

**B. To securely authenticate Databricks to Azure Storage using a Managed Identity** ✅ Correct

The Access Connector provides a Managed Identity.

Benefits:

- No storage account keys

- No passwords

- Secure authentication

- Azure-managed credentials

Flow:

Databricks\
↓\
Access Connector\
↓\
Managed Identity\
↓\
ADLS Gen2

**C. To configure SQL Warehouses** ❌ Incorrect

- SQL Warehouses are compute resources.

**D. To manage notebook permissions** ❌ Incorrect

- Notebook permissions are handled separately.

**E. To create Unity Catalog schemas** ❌ Incorrect

- Schemas are created after Unity Catalog is configured.

**Key Concept**

Access Connector = Secure identity for Azure Storage.

# [README](./../../../README.md)
