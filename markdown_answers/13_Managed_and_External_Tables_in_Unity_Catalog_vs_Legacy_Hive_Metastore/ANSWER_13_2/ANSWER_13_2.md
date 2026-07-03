# ANSWER 13 2

**Question 2**

**Which components are required to register an External Location in Unity Catalog?**

**A. Catalog and Schema** ❌ Incorrect

- Catalogs and schemas organize database objects.

- They do not define external storage.

**B. Cluster and Notebook** ❌ Incorrect

- These execute code.

- They are not part of an External Location.

**C. ADLS storage path, Storage Credential, and Managed Identity (Access Connector)** ✅ Correct

An External Location combines:

1.  **Cloud Storage Path**

Example:

abfss://finance@storageaccount.dfs.core.windows.net/

2.  **Storage Credential**

Contains authentication information.

3.  **Managed Identity (Access Connector)**

Allows secure Azure authentication without passwords.

Flow:

ADLS Path\
+\
Storage Credential\
+\
Managed Identity\
↓\
External Location

**D. Delta Table and Volume** ❌ Incorrect

- These are data objects, not External Location components.

**E. Metastore and Workspace** ❌ Incorrect

- These are administrative components.

**Memory Trick**

External Location =

WHERE\
(Storage URL)\
\
+\
\
HOW\
(Storage Credential)\
\
+\
\
WHO\
(Managed Identity)

------------------------------------------------------------------------

# [README](./../../../README.md)
