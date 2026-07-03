# ANSWER 11 6

**Question 6**

**Why might an existing compute cluster display the error "Unity Catalog is not enabled on this cluster"?**

**A. The cluster has Photon disabled.** ❌ Incorrect

- Photon improves performance.

- It has nothing to do with Unity Catalog support.

**B. The cluster was created before Unity Catalog was enabled and needs to be updated.** ✅ Correct

This is common.

Example:

Monday\
Cluster Created\
\
Tuesday\
Unity Catalog Enabled\
\
Wednesday\
Old Cluster\
↓\
\
Error

Solution:

- Restart cluster

- Edit cluster

- Or create a new UC-enabled cluster

**C. The storage account has insufficient capacity.** ❌ Incorrect

- Storage capacity does not determine Unity Catalog support.

**D. The catalog does not contain any tables.** ❌ Incorrect

- Empty catalogs do not cause this error.

**E. The cluster uses too many worker nodes.** ❌ Incorrect

- Worker count is unrelated.

**Key Concept**

Old Cluster

↓

Doesn't know Unity Catalog exists

# [README](./../../../README.md)
