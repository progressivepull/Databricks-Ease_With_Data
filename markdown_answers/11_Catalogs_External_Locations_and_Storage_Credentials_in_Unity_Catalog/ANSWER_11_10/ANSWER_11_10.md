# ANSWER 11 10

**Question 10**

**What is the effect of executing the command below?**

DROP CATALOG DevSQL CASCADE;

**A. Deletes only the catalog metadata while preserving all objects.** ❌ Incorrect

- CASCADE deletes much more than metadata.

**B. Deletes the catalog but leaves schemas and tables intact.** ❌ Incorrect

- Without CASCADE, the command would fail if objects still exist.

- CASCADE explicitly removes dependent objects.

**C. Recursively deletes the catalog and all contained schemas, tables, views, and other objects.** ✅ Correct

CASCADE means:

Delete everything underneath.

Example:

DevSQL\
├── default\
│ ├── Orders\
│ ├── Customers\
│ └── SalesView\
│\
└── Analytics\
├── Reports\
└── Functions

After:

DROP CATALOG DevSQL CASCADE;

Everything is removed.

**D. Archives the catalog for later recovery.** ❌ Incorrect

- SQL DROP permanently removes the catalog and its objects.

- It does not archive them.

**E. Converts the catalog into an external catalog.** ❌ Incorrect

- DROP deletes; it does not convert object types.

**Memory Trick**

Think of CASCADE as a domino effect:

Delete Catalog\
\
↓\
\
Delete Schemas\
\
↓\
\
Delete Tables\
\
↓\
\
Delete Views\
\
↓\
\
Delete Functions\
\
↓\
\
Delete Volumes

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| Managed storage priority | **Schema → Catalog → Metastore** |
| If no schema/catalog location exists | Use the **Metastore Managed Location** |
| Why assign catalog managed locations? | Separate storage for governance, isolation, and compliance |
| Default schemas in a new catalog | **default** and **information_schema** |
| DESCRIBE CATALOG EXTENDED | Displays catalog metadata (owner, comments, managed storage, properties, etc.) |
| "Unity Catalog is not enabled on this cluster" | The cluster was typically created before Unity Catalog was enabled and must be updated or recreated |
| Storage Credential | Securely authenticates Unity Catalog to cloud storage (often using a Managed Identity) |
| External Location | **Cloud Storage URL + Storage Credential** |
| Catalog with managed location | Managed tables are stored in the catalog's location unless a schema-level location overrides it |
| DROP CATALOG ... CASCADE | Recursively deletes the catalog and all contained schemas, tables, views, functions, volumes, and other dependent objects |

# [README](./../../../README.md)
