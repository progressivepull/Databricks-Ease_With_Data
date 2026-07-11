# ANSWER 25 3

**Question 3**

**Which feature ensures that Auto Loader does not process the same file more than once?**

**A. Time Travel ❌ Incorrect**

Time Travel lets you query older versions of Delta tables.

Example:

SELECT \* FROM sales VERSION AS OF 5;

It has nothing to do with ingestion.

------------------------------------------------------------------------

**B. Delta Cache ❌ Incorrect**

Delta Cache speeds up reads.

It does not track processed files.

**C. Exactly-once processing with checkpoints and RocksDB ✅ Correct**

Auto Loader stores information inside the checkpoint directory.

It records:

- processed files

- offsets

- stream progress

- RocksDB database

Workflow:

New File

↓

Processed?

↓

Yes → Skip

No → Load

That's exactly-once processing.

------------------------------------------------------------------------

**D. Partition Pruning ❌ Incorrect**

Partition pruning reduces the amount of data scanned during queries.

It does not affect ingestion.

------------------------------------------------------------------------

**E. Z-Ordering ❌ Incorrect**

Z-Ordering improves query performance.

It doesn't prevent duplicate ingestion.

------------------------------------------------------------------------

**Why C is correct**

Checkpoints + RocksDB remember every processed file, preventing duplicates.

------------------------------------------------------------------------

# [README](./../../../README.md)
