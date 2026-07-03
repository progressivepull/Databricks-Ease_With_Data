# ANSWER 11 1

**Question 1**

**When a managed table is created in Unity Catalog, which managed location has the highest priority for storing its data?**

**A. Metastore Managed Location** ❌ Incorrect

- The metastore managed location is the **fallback** location.

- It is only used when neither the schema nor the catalog has its own managed location.

- Think of it as the "default storage" for the entire metastore.

**B. Catalog Managed Location** ❌ Incorrect

- A catalog can have its own managed storage location.

- However, if the schema also has a managed location, the schema takes precedence.

- Therefore, the catalog is **second in priority**, not first.

**C. Schema Managed Location** ✅ Correct

This is the highest priority.

When creating a managed table, Unity Catalog checks storage locations in this order:

1\. Schema Managed Location ← Highest Priority\
2. Catalog Managed Location\
3. Metastore Managed Location

Example:

Metastore\
└── Sales Catalog\
└── Orders Schema\
└── Managed Location = ADLS/orders/\
\
New table\
↓\
Stored in Orders Schema location

**D. External Location** ❌ Incorrect

- External Locations are used for **external tables**, not managed tables.

- Managed tables always use managed storage.

**E. Storage Credential** ❌ Incorrect

- Storage Credentials contain authentication information.

- They do **not** specify where data is stored.

**Memory Trick**

Remember the storage priority:

Schema\
↓\
Catalog\
↓\
Metastore

# [README](./../../../README.md)
