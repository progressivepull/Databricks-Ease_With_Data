# ANSWER 24 3

**Question 3**

**How does Auto Loader achieve exactly-once processing?**

**A. By deleting processed files after ingestion** ❌ Incorrect\
Auto Loader does **not** delete source files.

Keeping source files allows:

- auditing

- replaying

- backup

------------------------------------------------------------------------

**B. By storing processed file metadata in a checkpoint directory using RocksDB** ✅ Correct

Inside the checkpoint directory Auto Loader stores:

- processed files

- progress

- RocksDB database

- offsets

- state

When restarted:

Checkpoint

↓

Already processed?

↓

Yes → Skip

No → Load

That's exactly-once processing.

------------------------------------------------------------------------

**C. By renaming processed files with a timestamp** ❌ Incorrect

Auto Loader never renames files.

------------------------------------------------------------------------

**D. By loading every file twice and comparing results** ❌ Incorrect

That would be inefficient.

Auto Loader reads each file once.

------------------------------------------------------------------------

**E. By requiring manual tracking of processed files** ❌ Incorrect

Everything is automatic.

------------------------------------------------------------------------

**Why B is correct**

The checkpoint maintains file history using RocksDB.

------------------------------------------------------------------------

# [README](./../../../README.md)
