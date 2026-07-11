# ANSWER 27 9

**Question 9**

**What information is stored in Streaming Table checkpoints?**

**A. User login credentials and cluster passwords ❌ Incorrect**

- Checkpoints never store security credentials.

------------------------------------------------------------------------

**B. Dashboard layouts and notebook comments ❌ Incorrect**

- Dashboards and notebook comments are unrelated to streaming checkpoints.

------------------------------------------------------------------------

**C. Processed records, stream offsets, and processing progress used for incremental execution. ✅ Correct**

Checkpoint contents include:

- processed file information

- stream offsets

- progress metadata

- state information

These allow the stream to resume exactly where it stopped.

Checkpoint

├── Offsets

├── Progress

├── State

└── Processed records

------------------------------------------------------------------------

**D. SQL query history only ❌ Incorrect**

- Query history is stored elsewhere, not in checkpoints.

------------------------------------------------------------------------

**E. Unity Catalog access policies only ❌ Incorrect**

- Access policies belong to Unity Catalog.

------------------------------------------------------------------------

**Why C is correct**

Checkpoints preserve the streaming state required for reliable, incremental processing and recovery.

------------------------------------------------------------------------

# [README](./../../../README.md)
