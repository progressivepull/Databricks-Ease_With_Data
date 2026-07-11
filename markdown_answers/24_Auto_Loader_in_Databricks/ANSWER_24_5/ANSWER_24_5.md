# ANSWER 24 5

**Question 5**

**Which Auto Loader option specifies where inferred schemas are stored?**

**A. cloudFiles.checkpointPath** ❌ Incorrect

There is no Auto Loader option called:

cloudFiles.checkpointPath

Streaming uses:

checkpointLocation

not this option.

------------------------------------------------------------------------

**B. cloudFiles.schemaHints** ❌ Incorrect

Schema hints override data types.

They do not store schemas.

**C. cloudFiles.schemaLocation** ✅ Correct

Example:

.option("cloudFiles.schemaLocation",

"/mnt/schema")

This location stores inferred schemas.

------------------------------------------------------------------------

**D. mergeSchema** ❌ Incorrect

Used for Delta schema evolution.

Not schema storage.

------------------------------------------------------------------------

**E. cloudFiles.useNotifications** ❌ Incorrect

Controls notification mode.

Nothing to do with schema storage.

------------------------------------------------------------------------

**Why C is correct**

Schema inference information is persisted in the location specified by cloudFiles.schemaLocation.

------------------------------------------------------------------------

# [README](./../../../README.md)
