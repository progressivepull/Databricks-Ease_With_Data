# EXPLANATION 27 4

**Question 4**

**Why are Streaming Tables efficient for incremental ETL?**

**Correct Answer:** **B. They process only new data by remembering previously processed records through checkpoints.**

**Explanation**

Streaming Tables maintain **checkpoint information**, which stores:

- Stream offsets

- Processing state

- Progress information

When the pipeline runs again, only newly arrived data is processed.

**Why the Correct Answer is Correct**

Checkpointing enables:

- Exactly-once processing

- Fault recovery

- Incremental execution

- Better performance

**Why the Other Answers Are Wrong**

Other options imply that every execution scans all source data.

**YouTube Video**\
<https://www.youtube.com/watch?v=iqf_QHC7tgQ>

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=iqf_QHC7tgQ>

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+Streaming+Table+checkpoints

------------------------------------------------------------------------

# [README](./../../../README.md)
