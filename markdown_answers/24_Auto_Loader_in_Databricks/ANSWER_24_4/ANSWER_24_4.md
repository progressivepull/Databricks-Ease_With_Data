# ANSWER 24 4

**Question 4**

**What is the primary purpose of the checkpoint directory?**

**A. To store Delta Lake transaction logs only** ❌ Incorrect

Delta transaction logs live in:

\_delta_log

Checkpoint is different.

------------------------------------------------------------------------

**B. To cache Spark executors for faster processing** ❌ Incorrect

Spark executor memory is temporary.

Not stored in checkpoints.

------------------------------------------------------------------------

**C. To store progress, schema information, processed file metadata, and RocksDB data** ✅ Correct

Checkpoint stores:

- streaming progress

- offsets

- processed files

- schema metadata

- RocksDB database

Everything needed to restart safely.

------------------------------------------------------------------------

**D. To permanently archive source files after processing** ❌ Incorrect

Source files remain where they are.

------------------------------------------------------------------------

**E. To store Unity Catalog permissions** ❌ Incorrect

Permissions belong to Unity Catalog.

------------------------------------------------------------------------

**Why C is correct**

Checkpoint = Auto Loader's memory.

Without it, Auto Loader wouldn't know what it already processed.

------------------------------------------------------------------------

# [README](./../../../README.md)
