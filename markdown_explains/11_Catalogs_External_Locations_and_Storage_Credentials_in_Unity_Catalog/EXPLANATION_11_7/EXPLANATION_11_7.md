# EXPLANATION 11 7

**Question 7**

**What is the primary purpose of a Storage Credential in Unity Catalog?**

**Correct Answer:**\
✅ **To securely connect Unity Catalog to cloud storage using a Managed Identity**

**Explanation**

A **Storage Credential** stores authentication information.

Azure example:

Unity Catalog\
\
↓\
\
Storage Credential\
\
↓\
\
Managed Identity\
\
↓\
\
Azure Storage

Instead of storing:

- Passwords

- Storage Keys

- Connection Strings

Unity Catalog uses Azure Managed Identity (or equivalent cloud identity services) to authenticate securely.

This improves security and follows cloud identity best practices.

**YouTube**

**Unity Catalog Storage Credentials**

https://www.youtube.com/results?search_query=Unity+Catalog+Storage+Credential

------------------------------------------------------------------------

# [README](./../../../README.md)
