# EXPLANATION 11 6

**Question 6**

**Why might an existing compute cluster display the error "Unity Catalog is not enabled on this cluster"?**

**Correct Answer:**\
✅ **The cluster was created before Unity Catalog was enabled and needs to be updated.**

**Explanation**

Clusters created before Unity Catalog was enabled may not support Unity Catalog.

Example:

Monday\
\
Create Cluster\
\
↓\
\
Tuesday\
\
Enable Unity Catalog\
\
↓\
\
Wednesday\
\
Run Notebook\
\
↓\
\
Error

Solution:

- Restart the cluster (if applicable)

- Edit and update the cluster configuration

- Or create a new Unity Catalog-compatible cluster

Databricks Runtime versions and cluster access modes also need to support Unity Catalog.

**YouTube**

**Unity Catalog Cluster Configuration**

https://www.youtube.com/results?search_query=Unity+Catalog+Cluster

------------------------------------------------------------------------

# [README](./../../../README.md)
