# EXPLANATION 17 8

**Question 8**

**What additional component is required when creating an External Volume?**

**Correct Answer:**\
✅ **A LOCATION pointing to external cloud storage**

**Explanation**

Example:

CREATE EXTERNAL VOLUME images\
\
LOCATION\
\
'abfss://media@storage.dfs.core.windows.net/images/';

The LOCATION tells Unity Catalog where the files already exist.

Typical storage:

- ADLS Gen2

- Amazon S3

- Google Cloud Storage

External Volumes reference customer-owned cloud storage rather than Unity Catalog-managed storage.

**Architecture**

External Volume\
\
↓\
\
LOCATION\
\
↓\
\
Cloud Storage

**YouTube**

**External Volumes**

https://www.youtube.com/results?search_query=Unity+Catalog+External+Volume

# [README](./../../../README.md)
