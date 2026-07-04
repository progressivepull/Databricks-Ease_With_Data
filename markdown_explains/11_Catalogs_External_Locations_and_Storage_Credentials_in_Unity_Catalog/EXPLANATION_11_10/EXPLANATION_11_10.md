# EXPLANATION 11 10

**Question 10**

**What is the effect of executing the command?**

DROP CATALOG DevSQL CASCADE;

**Correct Answer:**\
✅ **Recursively deletes the catalog and all contained schemas, tables, views, and other objects.**

**Explanation**

The keyword **CASCADE** means:

Delete everything contained inside the catalog.

Example:

DevSQL\
\
├── default\
\
│ ├── Orders\
\
│ ├── Customers\
\
│ └── Views\
\
├── Analytics\
\
│ ├── Reports\
\
│ └── Functions\
\
└── Volumes

After:

DROP CATALOG DevSQL CASCADE;

Everything shown above is removed.

Without CASCADE, the command fails if the catalog still contains objects.

Because this operation can permanently remove many objects, it should be used with caution.

**YouTube**

**Unity Catalog SQL Administration**

https://www.youtube.com/results?search_query=Unity+Catalog+SQL+Administration

------------------------------------------------------------------------

**Recommended YouTube Playlists**

If you're learning Unity Catalog storage, governance, and administration, these playlists cover these topics in depth:

1.  **Official Databricks – Unity Catalog**

    - https://www.youtube.com/results?search_query=Databricks+Unity+Catalog

2.  **Unity Catalog Tutorial**

    - https://www.youtube.com/results?search_query=Unity+Catalog+Tutorial

3.  **Azure Databricks Administration**

    - https://www.youtube.com/results?search_query=Azure+Databricks+Administration

4.  **Unity Catalog Storage Credentials & External Locations**

    - https://www.youtube.com/results?search_query=Unity+Catalog+Storage+Credential

5.  **Azure Databricks Full Course**

    - https://www.youtube.com/results?search_query=Azure+Databricks+Full+Course

# [README](./../../../README.md)
