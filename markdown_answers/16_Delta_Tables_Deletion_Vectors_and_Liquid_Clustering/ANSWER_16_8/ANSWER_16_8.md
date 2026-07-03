# ANSWER 16 8

**Question 8**

**In which scenario is Liquid Clustering especially recommended?**

**A. Small datasets with low-cardinality columns** ❌ Incorrect

- Small datasets usually don't benefit much.

**B. Tables containing only a few rows** ❌ Incorrect

- Clustering overhead isn't worthwhile.

**C. Large datasets with high-cardinality columns and frequent filtering or joins** ✅ Correct

Examples:

- Customer IDs

- Invoice Numbers

- Transaction IDs

These columns have many unique values.

Queries like:

WHERE customer_id = 123456

benefit significantly.

**D. Tables that never receive new data** ❌ Incorrect

- Static tables don't benefit much from automatic reclustering.

**E. Temporary views only** ❌ Incorrect

- Views don't store data.

**Memory Trick**

Large Table

- 

Many Unique Values

↓

Liquid Clustering

# [README](./../../../README.md)
