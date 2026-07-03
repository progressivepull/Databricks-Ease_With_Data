# ANSWER 11 9

**Question 9**

**What happens when a catalog is created with its own managed location?**

**A. Managed tables are still stored in the metastore location.** ❌ Incorrect

- The catalog's location overrides the metastore.

**B. Managed tables are stored under the catalog's managed storage path.** ✅ Correct

Example:

Catalog\
\
Managed Location:\
/storage/finance

New tables automatically go here unless the schema overrides it.

Priority:

Schema\
\
↓\
\
Catalog\
\
↓\
\
Metastore

**C. Unity Catalog is disabled for that catalog.** ❌ Incorrect

- Unity Catalog remains fully enabled.

**D. The catalog can no longer contain schemas.** ❌ Incorrect

- Schemas are still created normally.

**E. External Locations are no longer required.** ❌ Incorrect

- External Locations are still needed for external tables.

**Key Concept**

Catalog Managed Location

↓

All managed tables use it

Unless the schema specifies a different location.

# [README](./../../../README.md)
