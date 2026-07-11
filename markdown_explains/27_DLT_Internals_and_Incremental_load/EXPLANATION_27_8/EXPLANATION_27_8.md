# EXPLANATION 27 8

**Question 8**

**Where is the physical data for DLT Streaming Tables and Materialized Views actually stored?**

**Correct Answer:** **C. In hidden Delta tables within the Databricks Internal Catalog managed by DLT.**

**Explanation**

Although users query Streaming Tables and Materialized Views through Unity Catalog, DLT maintains internal Delta tables and metadata that support pipeline processing. These internal objects are managed by Databricks and are generally hidden from normal users.

**Why the Correct Answer is Correct**

The internal storage allows Databricks to efficiently manage refreshes, lineage, and incremental processing.

**Why the Other Answers Are Wrong**

The physical data is not stored only in notebook memory or external metadata files.

**YouTube Video**\
<https://www.youtube.com/watch?v=WREJAbBAgv0>

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=WREJAbBAgv0>

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+internal+catalog+Delta+Live+Tables

------------------------------------------------------------------------

# [README](./../../../README.md)
