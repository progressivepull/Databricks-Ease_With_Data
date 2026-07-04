# EXPLANATION 13 2

**Question 2**

**Which components are required to register an External Location in Unity Catalog?**

**Correct Answer:**\
✅ **ADLS storage path, Storage Credential, and Managed Identity (Access Connector)**

**Explanation**

An **External Location** combines three important pieces:

**1. Storage Path**

Example:

abfss://finance@storage.dfs.core.windows.net/

**2. Storage Credential**

Contains authentication information.

**3. Managed Identity (Access Connector)**

Allows Unity Catalog to securely access Azure Storage without passwords.

Architecture:

Storage URL\
+\
Storage Credential\
+\
Managed Identity\
↓\
External Location

Once created, external tables and external volumes can reuse this External Location.

**YouTube**

**Unity Catalog Storage Credentials & External Locations**

https://www.youtube.com/results?search_query=Unity+Catalog+Storage+Credential

# [README](./../../../README.md)
