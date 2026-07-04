# EXPLANATION 16 8

**Question 8**

**In which scenario is Liquid Clustering especially recommended?**

**Correct Answer:**\
✅ **Large datasets with high-cardinality columns and frequent filtering or joins**

**Explanation**

Examples of high-cardinality columns:

- Customer ID

- Invoice Number

- Order ID

- Transaction ID

Example query:

SELECT \*\
\
FROM sales\
\
WHERE invoice_number = 123456;

Liquid Clustering organizes data so these queries scan fewer files.

Databricks recommends Liquid Clustering especially for:

- Large, fast-growing tables

- High-cardinality filter columns

- Frequent joins

- Changing query patterns

**YouTube**

**Liquid Clustering Best Practices**

https://www.youtube.com/results?search_query=Databricks+Liquid+Clustering+Best+Practices

# [README](./../../../README.md)
