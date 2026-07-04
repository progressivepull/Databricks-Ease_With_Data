# EXPLANATION 17 10

**Question 10**

**What happens when an External Volume is dropped?**

**Correct Answer:**\
✅ **Only the metadata is removed, while the files remain in external storage.**

**Explanation**

External Volumes point to customer-owned cloud storage.

Example:

Azure Storage\
\
images/\
\
videos/\
\
pdfs/

After:

DROP VOLUME media;

Result:

Metadata:

❌ Removed

Files:

✅ Remain

Because the files are owned by the customer, Unity Catalog does not delete them.

This mirrors the behavior of External Tables.

**Comparison**

| **Managed Volume** | **External Volume** |
|--------------------|---------------------|
| Files deleted      | Files remain        |
| Metadata deleted   | Metadata deleted    |

**YouTube**

**External Volume Tutorial**

https://www.youtube.com/results?search_query=Unity+Catalog+External+Volume

**Recommended YouTube Playlists**

These playlists cover Unity Catalog Volumes, managed storage, and external storage concepts:

1.  **Official Databricks – Unity Catalog**

    - https://www.youtube.com/results?search_query=Databricks+Unity+Catalog

2.  **Unity Catalog Volumes**

    - https://www.youtube.com/results?search_query=Unity+Catalog+Volumes

3.  **Storage Credentials & External Locations**

    - https://www.youtube.com/results?search_query=Unity+Catalog+Storage+Credential

4.  **Azure Databricks Full Course**

    - https://www.youtube.com/results?search_query=Azure+Databricks+Full+Course

5.  **DBUtils Tutorial**

    - https://www.youtube.com/results?search_query=Databricks+DBUtils+Tutorial

# [README](./../../../README.md)
