# ANSWER 11 7

**Question 7**

**What is the primary purpose of a Storage Credential in Unity Catalog?**

**A. To store Delta table metadata** ❌ Incorrect

- Metadata is stored in the Unity Catalog metastore.

**B. To securely connect Unity Catalog to cloud storage using a Managed Identity** ✅ Correct

Storage Credential = Authentication

It tells Unity Catalog:

"Here's how to securely access storage."

Azure example:

Managed Identity\
\
↓\
\
Storage Credential\
\
↓\
\
ADLS Gen2

No passwords or storage keys are required.

**C. To create schemas automatically** ❌ Incorrect

- Schemas are created with SQL commands.

**D. To replace Azure Storage Accounts** ❌ Incorrect

- Storage Credentials connect to storage accounts.

- They do not replace them.

**E. To execute SQL queries** ❌ Incorrect

- Compute clusters execute SQL.

**Memory Trick**

Storage Credential = Identity

Not Storage

# [README](./../../../README.md)
