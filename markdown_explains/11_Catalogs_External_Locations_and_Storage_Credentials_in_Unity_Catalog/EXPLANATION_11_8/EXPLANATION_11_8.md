# EXPLANATION 11 8

**Question 8**

**Which two components make up an External Location?**

**Correct Answer:**\
✅ **Cloud storage URL and Storage Credential**

**Explanation**

An **External Location** combines:

**Cloud Storage URL**

Example:

abfss://finance@storage.dfs.core.windows.net/

and

**Storage Credential**

Which securely authenticates access.

Architecture:

Storage URL\
\
+\
\
Storage Credential\
\
↓\
\
External Location

Once created, external tables and external volumes can reference this External Location rather than repeatedly specifying credentials.

**YouTube**

**External Locations Explained**

https://www.youtube.com/results?search_query=Unity+Catalog+External+Location

------------------------------------------------------------------------

# [README](./../../../README.md)
