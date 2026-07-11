# ANSWER 42 6

**Question 6**

**What is the effect of setting includeExistingFiles = false when creating a Streaming Table?**

**A. All existing files are reprocessed during every refresh.** ❌ Incorrect

- That is the opposite of what happens.

**B. Previously processed files are ignored, and only newly arriving files are processed.** ✅ Correct

- Existing files are skipped.

- Only new files are ingested after the Streaming Table begins monitoring.

Example:

Before:

file1.csv

file2.csv

file3.csv

After enabling:

file4.csv

file5.csv

Only:

- file4

- file5

are processed.

**C. Streaming Tables cannot be refreshed incrementally.** ❌ Incorrect

- Incremental refresh is their primary feature.

**D. The Streaming Table performs a full refresh every hour.** ❌ Incorrect

- Full refreshes happen only when explicitly requested.

**E. Materialized Views are refreshed automatically.** ❌ Incorrect

- This setting has nothing to do with Materialized Views.

**Key Concept**

**includeExistingFiles = false → Ignore old files; process only new arrivals.**

# [README](./../../../README.md)
