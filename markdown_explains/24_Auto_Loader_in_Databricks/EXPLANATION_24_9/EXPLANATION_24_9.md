# EXPLANATION 24 9

**Question 9**

**Which trigger should be used when Auto Loader needs to process all currently available files and then stop automatically?**

**Correct Answer:** **C. .trigger(availableNow=True)**

**Explanation**

availableNow is ideal for scheduled or batch-style ingestion.

Instead of running continuously, it:

1.  Processes all files currently available.

2.  Stops automatically when finished.

This pattern is often used in daily or hourly jobs to minimize compute costs.

**YouTube**

- https://www.youtube.com/results?search_query=Databricks+availableNow+trigger

- https://www.youtube.com/results?search_query=Structured+Streaming+availableNow

------------------------------------------------------------------------

# [README](./../../../README.md)
