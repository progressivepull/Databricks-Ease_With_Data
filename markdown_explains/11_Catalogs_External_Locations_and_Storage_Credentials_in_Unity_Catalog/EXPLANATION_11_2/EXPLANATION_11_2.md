# EXPLANATION 11 2

**Question 2**

**If neither a schema nor a catalog has a managed location configured, where will managed table data be stored?**

**Correct Answer:**\
✅ **Metastore Managed Location**

**Explanation**

If:

- No schema managed location exists

- No catalog managed location exists

Unity Catalog falls back to the **Metastore Managed Location**.

Storage priority:

Schema\
↓\
Catalog\
↓\
Metastore

This default location ensures that managed tables always have a valid storage destination.

**Example**

Metastore\
Managed Storage\
\
↓\
\
New Table\
\
↓\
\
Stored Here

**YouTube**

**Unity Catalog Storage Hierarchy**

https://www.youtube.com/results?search_query=Unity+Catalog+Managed+Location

------------------------------------------------------------------------

# [README](./../../../README.md)
