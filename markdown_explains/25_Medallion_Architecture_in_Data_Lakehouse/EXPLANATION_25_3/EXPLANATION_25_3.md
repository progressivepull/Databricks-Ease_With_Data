# EXPLANATION 25 3

**Question 3**

**How does Auto Loader achieve exactly-once processing?**

**Correct Answer**

✅ **B. By storing processed file metadata in a checkpoint directory using RocksDB**

**Explanation**

Auto Loader keeps a database of every processed file.

That database is:

- RocksDB

- stored inside the checkpoint directory

When restarted, Auto Loader asks:

"Have I processed this file already?"

If yes:

Skip it.

If no:

Load it.

That's how duplicate processing is avoided.

**Easy Memory Trick**

Checkpoint → RocksDB → File History

**YouTube**

https://www.youtube.com/results?search_query=Databricks+Auto+Loader+checkpoint+RocksDB

------------------------------------------------------------------------

# [README](./../../../README.md)
