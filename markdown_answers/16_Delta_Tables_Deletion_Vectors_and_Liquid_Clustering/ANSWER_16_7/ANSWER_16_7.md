# ANSWER 16 7

**Question 7**

**What is the primary advantage of Liquid Clustering over traditional partitioning and Z-Ordering?**

**A. It completely eliminates Delta tables.** ❌ Incorrect

- Liquid Clustering is a Delta Lake feature.

**B. It automatically reorganizes data as new records arrive, reducing manual maintenance.** ✅ Correct

Traditional approach:

Load Data\
\
↓\
\
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

Liquid Clustering:

Load Data\
\
↓\
\
Automatically Maintains Clustering

Far less maintenance.

**C. It requires more manual repartitioning.** ❌ Incorrect

- The opposite is true.

**D. It works only with JSON files.** ❌ Incorrect

- Works with Delta tables.

**E. It permanently disables OPTIMIZE.** ❌ Incorrect

- OPTIMIZE is still used with Liquid Clustering.

**Key Concept**

Liquid Clustering

↓

Automatic Maintenance

# [README](./../../../README.md)
