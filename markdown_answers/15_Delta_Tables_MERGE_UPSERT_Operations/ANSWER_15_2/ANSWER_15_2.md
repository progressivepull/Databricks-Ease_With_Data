# ANSWER 15 2

**Question 2**

**Which other names are commonly used for the MERGE operation?**

**A. VACUUM and OPTIMIZE** ❌ Incorrect

- VACUUM removes old files.

- OPTIMIZE reorganizes files.

- Neither updates business records.

**B. UPSERT and Slowly Changing Dimension (SCD) Type 1** ✅ Correct

MERGE is commonly called an **UPSERT** because it:

- Updates existing rows.

- Inserts new rows.

Many ETL pipelines also use MERGE to implement **Slowly Changing Dimension (SCD) Type 1**, where old values are overwritten instead of preserved.

Example:

Customer\
\
Old Address\
↓\
\
New Address\
\
MERGE\
\
↓\
\
Address Updated

**C. Deep Clone and Shallow Clone** ❌ Incorrect

- These duplicate tables.

- They do not merge records.

**D. Time Travel and History Tracking** ❌ Incorrect

- Time Travel lets you query previous versions.

- It is unrelated to MERGE logic.

**E. Auto Loader and COPY INTO** ❌ Incorrect

- These ingest data.

- MERGE processes the data after it has been loaded.

**Key Concept**

UPSERT =

UPDATE\
\
or\
\
INSERT

------------------------------------------------------------------------

# [README](./../../../README.md)
