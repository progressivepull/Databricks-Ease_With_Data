# ANSWER 17 3

**Question 3**

**Where do Volumes fit within the Unity Catalog object hierarchy?**

**A. Above the Metastore** ❌ Incorrect

- Nothing is above the Metastore.

**B. Alongside Catalogs** ❌ Incorrect

- Volumes are much lower in the hierarchy.

**C. As siblings of Tables within a Schema** ✅ Correct

Hierarchy:

Metastore\
↓\
Catalog\
↓\
Schema\
├── Tables\
├── Views\
├── Functions\
└── Volume

Volumes live inside schemas exactly like tables.

**D. Under External Locations only** ❌ Incorrect

- Only External Volumes reference External Locations.

- Managed Volumes do not.

**E. Inside Storage Credentials** ❌ Incorrect

- Storage Credentials provide authentication.

- They do not contain Volumes.

------------------------------------------------------------------------

**Memory Trick**

Inside a Schema:

Table\
\
View\
\
Function\
\
Volume

------------------------------------------------------------------------

# [README](./../../../README.md)
