# EXPLANATION 42 6

**Question 6**

**What is the effect of setting includeExistingFiles = false when creating a Streaming Table?**

**Correct Answer:**\
**B. Previously processed files are ignored, and only newly arriving files are processed.**

**Why B is Correct**

When:

includeExistingFiles = false

the Streaming Table skips historical files and processes only files that arrive after the stream begins.

This is useful when:

- Existing data has already been loaded.

- Only future arrivals matter.

- Duplicate processing should be avoided.

**Why the other choices are wrong**

It does not delete existing files or reload all historical data.

**Memory Tip**

**False = Future Files Only**

**Individual YouTube Video**

Streaming Tables Incremental Processing

https://www.youtube.com/watch?v=lR1Q3F2M4qI

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Streaming+Tables+includeExistingFiles

------------------------------------------------------------------------

# [README](./../../../README.md)
