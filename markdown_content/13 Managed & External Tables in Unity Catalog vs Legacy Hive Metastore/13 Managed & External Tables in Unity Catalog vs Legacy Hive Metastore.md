# 13 Managed & External Tables in Unity Catalog vs Legacy Hive Metastore

**Managed & External Tables in Unity Catalog vs. Legacy Hive Metastore**

This lesson compares how **Managed Tables** and **External Tables** behave in **Unity Catalog** versus the legacy **Hive Metastore**. It also introduces the **UNDROP** feature, which allows recently dropped tables to be restored—a capability not available in the legacy Hive Metastore.

**Key Topics Covered**

**1. Preparing an External Storage Location**

Before creating an external table, the instructor creates a dedicated folder in Azure Data Lake Storage (ADLS) for storing external table data.

The directory structure is:

Storage Account\
└── data\
└── ADB\
└── external_tables

This folder serves as the root location for all Unity Catalog external tables.

**2. Creating an External Location**

After creating the ADLS folder, it must be registered in Unity Catalog as an **External Location**.

The External Location consists of:

- ADLS storage path

- Storage Credential

- Managed Identity (Azure Access Connector)

The instructor verifies the configuration using **Test Connection**, confirming that Databricks has permission to access the storage location.

**3. Creating a Managed Table**

A managed table is created inside:

- Catalog: **dev**

- Schema: **branch**

Characteristics of the managed table:

- Unity Catalog manages both metadata and data.

- No storage location is specified.

- Data is stored in the catalog's (or metastore's) managed storage location.

**4. Creating an External Table**

Next, an external table is created in the same catalog and schema.

Unlike the managed table, it specifies a storage location using:

LOCATION '\<external path\>'

Characteristics:

- Metadata is stored in Unity Catalog.

- Data is stored in the specified ADLS folder.

- Unity Catalog does not manage the physical data files.

**5. Viewing Table Properties**

Using:

DESCRIBE EXTENDED table_name;

the lesson compares both tables.

For the **Managed Table**:

- Table Type: **Managed**

- Storage Location: Unity Catalog managed storage

- Data stored under the metastore-managed location

For the **External Table**:

- Table Type: **External**

- Storage Location: User-defined ADLS path

**6. Verifying Physical Data Files**

The instructor confirms the physical storage locations:

**Managed Table**

- Stored in Unity Catalog's managed storage area

- Organized internally using a unique table ID

**External Table**

- Stored directly in the configured ADLS directory

- Files are visible in Azure Storage

This demonstrates that both table types have physical data files, but they reside in different locations.

**Managed Table Behavior in Hive Metastore**

Previously (Hive Metastore):

Dropping a managed table:

DROP TABLE managed_table;

immediately removed:

- Table metadata

- Physical data files

Recovery was not possible after the drop.

**Managed Table Behavior in Unity Catalog**

Unity Catalog changes this behavior.

After executing:

DROP TABLE managed_table;

the table disappears from Catalog Explorer, but the data files **remain temporarily**.

The files are retained for a recovery period rather than being deleted immediately.

This enables one of Unity Catalog's most valuable features: **UNDROP**.

**7. SHOW TABLES DROPPED**

Unity Catalog allows administrators to list recently dropped tables.

Example:

SHOW TABLES DROPPED IN branch;

The command displays:

- Dropped table names

- Table IDs

- Recovery eligibility

Only tables within the retention window appear.

**8. UNDROP TABLE**

A dropped table can be restored using:

UNDROP TABLE table_name;

After executing the command:

- Metadata is restored.

- The table reappears in Catalog Explorer.

- Existing data becomes immediately accessible.

No data needs to be reloaded.

**9. Retention Period**

Unity Catalog retains dropped managed tables for **7 days**.

During this period:

- Metadata can be restored.

- Data files remain available.

After the retention period expires, Databricks permanently removes the managed table data.

**10. External Table Recovery**

The same recovery capability applies to external tables.

When an external table is dropped:

- Metadata is removed.

- Physical data remains permanently in ADLS.

The table can be restored using either:

<span class="mark">UNDROP TABLE table_name;</span>

or

<span class="mark">UNDROP TABLE WITH ID table_id;</span>

Since Unity Catalog never deletes the external data files, recovery simply recreates the metadata.

**11. Unity Catalog Documentation**

The instructor references the Databricks documentation, which confirms:

- Dropped tables can be recovered within **7 days**.

- Managed tables retain their data during the recovery window.

- External table data is never automatically deleted because it resides in customer-managed storage.

**Hive Metastore vs. Unity Catalog**

| **Feature** | **Hive Metastore** | **Unity Catalog** |
|----|----|----|
| Managed table data deleted immediately | ✔ | ✘ |
| Managed table recoverable after drop | ✘ | ✔ (within 7 days) |
| External table data retained | ✔ | ✔ |
| UNDROP feature | ✘ | ✔ |
| Recover by Table ID | ✘ | ✔ |
| Centralized governance | ✘ | ✔ |

**Managed vs. External Tables in Unity Catalog**

| **Feature** | **Managed Table** | **External Table** |
|----|----|----|
| Metadata stored in Unity Catalog | ✔ | ✔ |
| Physical data managed by Unity Catalog | ✔ | ✘ |
| Data location specified manually | ✘ | ✔ |
| Data removed immediately after DROP | ✘ | ✘ |
| Metadata recoverable using UNDROP | ✔ | ✔ |
| Physical data retained after DROP | Temporarily (7-day recovery period) | Permanently |

**Key Takeaways**

- Unity Catalog continues to distinguish between **Managed Tables** and **External Tables**, but significantly improves recovery capabilities compared to the legacy Hive Metastore.

- **Managed Tables** store their data in Unity Catalog's managed storage, while **External Tables** store data in user-defined cloud storage locations.

- Unlike Hive Metastore, dropping a managed table in Unity Catalog does **not** immediately delete the underlying data. The data is retained during a **7-day recovery window**, allowing accidental deletions to be reversed.

- The **SHOW TABLES DROPPED** command lists recently deleted tables that are eligible for recovery.

- The **UNDROP TABLE** command restores a dropped table, including its metadata and access to its existing data.

- External tables can also be recovered using **UNDROP**, and because their data remains in customer-managed storage, only the metadata needs to be restored.

- Unity Catalog's recovery features provide an additional layer of protection against accidental data loss while maintaining centralized governance and metadata management.

# [README](./../../../README.md)
