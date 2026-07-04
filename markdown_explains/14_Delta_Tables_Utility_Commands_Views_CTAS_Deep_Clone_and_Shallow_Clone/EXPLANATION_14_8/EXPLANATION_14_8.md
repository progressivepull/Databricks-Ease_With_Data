# EXPLANATION 14 8

**Question 8**

**What is the main advantage of Deep Clone over CTAS?**

**Correct Answer:**\
✅ **It preserves metadata, schema, table properties, and data, creating a true replica.**

**Explanation**

Deep Clone creates a nearly complete copy of a Delta table.

Example:

CREATE TABLE finance.sales_backup\
\
DEEP CLONE finance.sales;

Deep Clone copies:

- Data

- Schema

- Table Properties

- Partitioning

- Metadata

Unlike CTAS, it is intended to create an independent replica of the original table. Databricks documents that deep clones copy both data and metadata, while shallow clones reference the original data files.

**Comparison**

| **CTAS**          | **Deep Clone**     |
|-------------------|--------------------|
| Copies Data       | Copies Data        |
| May lose metadata | Preserves metadata |
| Simple copy       | Full replica       |

**YouTube**

**Deep Clone vs CTAS**

https://www.youtube.com/results?search_query=Databricks+Deep+Clone

# [README](./../../../README.md)
