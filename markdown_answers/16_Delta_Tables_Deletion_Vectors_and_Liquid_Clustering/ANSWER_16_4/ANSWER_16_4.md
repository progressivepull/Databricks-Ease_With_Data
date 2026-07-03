# ANSWER 16 4

**Question 4**

**Which table property controls whether Deletion Vectors are enabled?**

**A. delta.enablePhoton** ❌ Incorrect

- Photon is the execution engine.

**B. delta.enableDeletionVectors** ✅ Correct

Example:

ALTER TABLE employees\
SET TBLPROPERTIES\
(\
'delta.enableDeletionVectors'='true'\
);

This turns the feature on.

**C. delta.autoOptimize** ❌ Incorrect

- Controls automatic optimization.

**D. delta.enableClusterBy** ❌ Incorrect

- Related to Liquid Clustering.

**E. delta.optimizeWrite** ❌ Incorrect

- Optimizes file writing.

**Memory Trick**

Deletion Vectors

↓

delta.enableDeletionVectors

# [README](./../../../README.md)
