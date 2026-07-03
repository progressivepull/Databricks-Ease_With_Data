# ANSWER 13 10

**Question 10**

**Which capability is available in Unity Catalog but not in the legacy Hive Metastore?**

**A. Managed tables** ❌ Incorrect

- Hive Metastore supports managed tables.

**B. External tables** ❌ Incorrect

- Hive Metastore also supports external tables.

**C. UNDROP TABLE for recovering dropped tables** ✅ Correct

This is a major enhancement in Unity Catalog.

Legacy Hive Metastore:

DROP TABLE\
\
↓\
\
Gone

Unity Catalog:

DROP TABLE\
\
↓\
\
Retention Period\
\
↓\
\
UNDROP TABLE\
\
↓\
\
Recovered

This greatly reduces the risk of accidental deletions.

**D. Delta Lake support** ❌ Incorrect

- Hive Metastore also supports Delta Lake.

**E. SQL queries** ❌ Incorrect

- SQL has always been supported.

**Key Concept**

One of Unity Catalog's biggest improvements over the legacy Hive Metastore is the ability to recover accidentally dropped managed tables using **UNDROP TABLE** during the retention period.

------------------------------------------------------------------------

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| External table prerequisite | Create a dedicated ADLS folder first |
| External Location requires | **ADLS path + Storage Credential + Managed Identity (Access Connector)** |
| Managed table storage | Unity Catalog automatically uses the schema, catalog, or metastore managed location |
| Managed vs. External | Managed = Unity Catalog manages storage; External = User specifies the storage location |
| Dropped managed table | Metadata is removed, but data is retained temporarily for recovery |
| List dropped tables | SHOW TABLES DROPPED IN schema_name |
| Recover a dropped table | UNDROP TABLE |
| Default recovery period | **7 days** |
| Dropped external table | Metadata is removed; physical data remains in the external storage location |
| Unity Catalog enhancement | UNDROP TABLE recovery capability, which was not available in the legacy Hive Metastore |

# [README](./../../../README.md)
