# ANSWER 17 2

**Question 2**

**Which prerequisites are required to use Volumes in Databricks?**

**A. Hive Metastore and Databricks Runtime 10.4 LTS** ❌ Incorrect

- Volumes are a **Unity Catalog feature**.

- Hive Metastore does not support Unity Catalog Volumes.

**B. Unity Catalog enabled and Databricks Runtime 13.3 LTS or later** ✅ Correct

Volumes require:

- Unity Catalog enabled

- Databricks Runtime **13.3 LTS or newer**

Without Unity Catalog:

No Volumes

**C. Photon enabled and SQL Warehouse** ❌ Incorrect

- Photon is optional.

- SQL Warehouses are unrelated.

**D. Azure Key Vault only** ❌ Incorrect

- Key Vault stores secrets.

- It is not a requirement for Volumes.

**E. Delta Live Tables enabled** ❌ Incorrect

- Delta Live Tables are pipeline tools.

------------------------------------------------------------------------

**Key Concept**

Volumes require:

Unity Catalog\
\
+\
\
DBR 13.3 LTS+

------------------------------------------------------------------------

# [README](./../../../README.md)
