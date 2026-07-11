# EXPLANATION 27 7

**Question 7**

**What happens when a dataset such as joined_silver is renamed to order_silver in the DLT notebook?**

**Correct Answer:** **C. DLT automatically removes the old dataset, creates the new one, and updates pipeline metadata.**

**Explanation**

Pipeline definitions are declarative. When a dataset definition changes, DLT updates the managed pipeline objects and metadata to reflect the new definition during the next pipeline update. Recent platform behavior has evolved so that inactive datasets may be retained in some scenarios, but the pipeline metadata is automatically updated to match the new definitions.

**Why the Correct Answer is Correct**

Developers modify only the notebook code; DLT synchronizes the pipeline state.

**Why the Other Answers Are Wrong**

The other options incorrectly imply manual metadata updates or manual table management.

**YouTube Video**\
<https://www.youtube.com/watch?v=WREJAbBAgv0>

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=WREJAbBAgv0>

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+DLT+rename+table

------------------------------------------------------------------------

# [README](./../../../README.md)
