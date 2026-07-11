# EXPLANATION 27 9

**Question 9**

**What information is stored in Streaming Table checkpoints?**

**Correct Answer:** **C. Processed records, stream offsets, and processing progress used for incremental execution.**

**Explanation**

Checkpoints record:

- Stream offsets

- Processing progress

- Execution state

- Information required for fault recovery

This allows pipelines to resume from the last successfully processed data instead of restarting.

**Why the Correct Answer is Correct**

Checkpointing enables exactly-once processing and efficient incremental execution.

**Why the Other Answers Are Wrong**

The incorrect options confuse checkpoints with the actual data or schema definitions.

**YouTube Video**\
<https://www.youtube.com/watch?v=iqf_QHC7tgQ>

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=iqf_QHC7tgQ>

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+Streaming+checkpoint+DLT

------------------------------------------------------------------------

# [README](./../../../README.md)
