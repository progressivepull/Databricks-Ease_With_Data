# ANSWER 09 9

**Question 9**

**Why can an external table be recreated after it has been dropped?**

**A. The metadata is automatically restored by Spark.** ❌ Incorrect

- Spark does not automatically recreate metadata.

**B. The table definition is stored in Azure Active Directory.** ❌ Incorrect

- Azure Active Directory manages identities, not table definitions.

**C. The physical data remains in the specified external storage location.** ✅ Correct

Example:

ADLS\
sales.delta

After:

DROP TABLE sales;

The files remain.

You can recreate the table:

CREATE TABLE sales\
USING DELTA\
LOCATION '/mnt/raw/sales'

The table works again because the data was never deleted.

**D. Unity Catalog recreates the table automatically.** ❌ Incorrect

- Recreation is a manual operation.

**E. Delta Lake permanently stores every dropped table.** ❌ Incorrect

- Delta Lake stores transaction history for existing tables, but it does not automatically restore dropped external table metadata.

**Key Concept**

External Table:

Metadata\
↓\
Deleted\
\
Files\
↓\
Remain

------------------------------------------------------------------------

# [README](./../../../README.md)
