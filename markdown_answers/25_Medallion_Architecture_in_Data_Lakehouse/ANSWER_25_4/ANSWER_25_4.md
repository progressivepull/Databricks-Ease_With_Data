# ANSWER 25 4

**Question 4**

**Which Auto Loader option specifies where inferred schemas and schema evolution metadata are stored?**

**A. cloudFiles.metadataLocation ❌ Incorrect**

No such Auto Loader option exists.

------------------------------------------------------------------------

**B. cloudFiles.schemaLocation ✅ Correct**

Example:

.option(

"cloudFiles.schemaLocation",

"/schemas/customer"

)

This stores:

- inferred schemas

- schema evolution history

- metadata needed for future runs

------------------------------------------------------------------------

**C. checkpointLocation ❌ Incorrect**

Checkpoint stores:

- stream progress

- offsets

- processed files

- RocksDB

It does **not** store inferred schemas.

**D. delta.schemaPath ❌ Incorrect**

Not a valid option.

------------------------------------------------------------------------

**E. schemaTrackingPath ❌ Incorrect**

Also not a valid Auto Loader option.

------------------------------------------------------------------------

**Why B is correct**

cloudFiles.schemaLocation is Auto Loader's schema repository.

------------------------------------------------------------------------

# [README](./../../../README.md)
