# EXPLANATION 27 3

**Question 3**

**When 10,000 new rows are added to the orders_raw table and the DLT pipeline is rerun, what happens?**

**Correct Answer:** **C. Only the new 10,000 order records are processed by the Streaming Table, and downstream layers are updated automatically.**

**Explanation**

Streaming Tables perform **incremental processing**.

Instead of reading the entire table again, DLT:

- Detects new records.

- Processes only those records.

- Updates downstream Silver and Gold datasets automatically.

**Why the Correct Answer is Correct**

Streaming Tables remember what has already been processed through checkpoints.

**Why the Other Answers Are Wrong**

The other answers incorrectly suggest that all historical data must be reprocessed.

**YouTube Video**\
<https://www.youtube.com/watch?v=iqf_QHC7tgQ>

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=iqf_QHC7tgQ>

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+Streaming+Tables+incremental+processing

------------------------------------------------------------------------

# [README](./../../../README.md)
