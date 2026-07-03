# ANSWER 16 10

**Question 10**

**What is one limitation when selecting clustering columns for Liquid Clustering?**

**A. Only one clustering column is allowed.** ❌ Incorrect

- Multiple clustering columns are supported.

**B. Clustering columns must always be numeric.** ❌ Incorrect

- Strings, dates, timestamps, and other supported data types can be used.

**C. Clustering columns must appear within the first 32 columns of the table.** ✅ Correct

This is an implementation limitation.

If a table has:

Column 1\
\
Column 2\
\
...\
\
Column 45

Column 45 cannot be selected for clustering unless the schema is changed so that it appears within the first 32 columns.

**D. Clustering can only be enabled during table creation.** ❌ Incorrect

- Existing tables can be altered:

ALTER TABLE ...\
CLUSTER BY (...)

**E. Clustering works only on managed tables.** ❌ Incorrect

- Liquid Clustering is supported for Delta tables regardless of whether they are managed or external, provided the feature requirements are met.

**Memory Trick**

Liquid Clustering Rule

↓

Clustering columns

↓

Must be in the **first 32 columns**.

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| Purpose of Deletion Vectors | Avoid rewriting entire Parquet files during DELETE operations by marking rows as deleted |
| Deleted rows with Deletion Vectors | Logically deleted (ignored by queries) until files are rewritten |
| Physically remove deleted rows | OPTIMIZE table_name; rewrites files without the deleted rows |
| Enable Deletion Vectors | delta.enableDeletionVectors table property |
| DESCRIBE HISTORY shows | Transaction details and operation metrics, including files rewritten and deletion vectors added |
| Minimum versions | Delta Lake **2.3+** and Databricks Runtime **12.2 LTS+** |
| Main advantage of Liquid Clustering | Automatically maintains data organization as data changes, reducing manual tuning |
| Best use case | Large Delta tables with high-cardinality columns that are frequently filtered or joined |
| Enable Liquid Clustering | ALTER TABLE table_name CLUSTER BY (column_name); |
| Clustering limitation | Selected clustering columns must be within the **first 32 columns** of the table |

# [README](./../../../README.md)
