# EXPLANATION 14 10

**Question 10**

**Which operation can negatively impact a Shallow Clone because it initially references the original table's data files?**

**Correct Answer:**\
✅ **VACUUM**

**Explanation**

Shallow Clones depend on the source table's files.

Example:

Original Table\
\
↓\
\
Data Files\
\
↑\
\
Shallow Clone

When:

VACUUM sales;

runs, old data files that are no longer needed by the source table may be permanently removed.

If the shallow clone still references those files, it may no longer function correctly.

Because of this relationship, Databricks recommends understanding the lifecycle of the source table before relying on shallow clones.

**YouTube**

**VACUUM and Delta Lake**

https://www.youtube.com/results?search_query=Databricks+VACUUM+Delta+Lake

**Recommended YouTube Playlists**

These playlists cover all of the concepts in Questions 1–10:

1.  **Official Databricks – Delta Lake & Unity Catalog**

    - https://www.youtube.com/results?search_query=Databricks+Delta+Lake+Unity+Catalog

2.  **Databricks SQL Tutorial**

    - https://www.youtube.com/results?search_query=Databricks+SQL+Tutorial

3.  **Delta Lake Deep Clone & Shallow Clone**

    - https://www.youtube.com/results?search_query=Databricks+Deep+Clone+Shallow+Clone

4.  **Azure Databricks Full Course**

    - https://www.youtube.com/results?search_query=Azure+Databricks+Full+Course

5.  **Delta Lake Complete Tutorial**

    - https://www.youtube.com/results?search_query=Delta+Lake+Tutorial

# [README](./../../../README.md)
