# EXPLANATION 13 10

**Question 10**

**Which capability is available in Unity Catalog but not in the legacy Hive Metastore?**

**Correct Answer:**\
✅ **UNDROP TABLE for recovering dropped tables**

**Explanation**

One of Unity Catalog's major improvements is the ability to recover accidentally dropped managed tables.

**Legacy Hive Metastore**

DROP TABLE\
\
↓\
\
Gone Forever

**Unity Catalog**

DROP TABLE\
\
↓\
\
Recovery Window\
\
↓\
\
UNDROP TABLE\
\
↓\
\
Recovered

This significantly reduces the risk of accidental data loss and is especially valuable in production environments.

**YouTube**

**Unity Catalog Features**

https://www.youtube.com/results?search_query=Unity+Catalog+Features

**Recommended YouTube Playlists**

If you're learning managed tables, external tables, and Unity Catalog storage, these playlists are excellent:

1.  **Official Databricks – Unity Catalog**

    - https://www.youtube.com/results?search_query=Databricks+Unity+Catalog

2.  **Unity Catalog External Tables**

    - https://www.youtube.com/results?search_query=Unity+Catalog+External+Tables

3.  **Managed vs External Tables**

    - https://www.youtube.com/results?search_query=Managed+vs+External+Tables+Databricks

4.  **Azure Data Lake Storage Gen2**

    - https://www.youtube.com/results?search_query=Azure+Data+Lake+Storage+Gen2

5.  **Azure Databricks Full Course**

    - https://www.youtube.com/results?search_query=Azure+Databricks+Full+Course

# [README](./../../../README.md)
