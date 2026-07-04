# EXPLANATION 16 7

**Question 7**

**What is the primary advantage of Liquid Clustering over traditional partitioning and Z-Ordering?**

**Correct Answer:**\
✅ **It automatically reorganizes data as new records arrive, reducing manual maintenance.**

**Explanation**

Traditional optimization often requires:

Partition\
\
↓\
\
OPTIMIZE\
\
↓\
\
ZORDER\
\
↓\
\
Repeat

Liquid Clustering automatically maintains the data layout based on clustering keys.

Benefits include:

- Less manual tuning

- Better query performance

- Easier maintenance

- Flexible clustering keys

Unlike traditional partitioning, clustering keys can be changed without rewriting all existing data.

**YouTube**

**Liquid Clustering**

https://www.youtube.com/results?search_query=Databricks+Liquid+Clustering

# [README](./../../../README.md)
