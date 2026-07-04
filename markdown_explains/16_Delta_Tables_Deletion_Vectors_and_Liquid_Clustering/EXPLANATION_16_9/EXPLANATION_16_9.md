# EXPLANATION 16 9

**Question 9**

**Which SQL command enables Liquid Clustering on an existing Delta table?**

**Correct Answer:**\
✅ **ALTER TABLE table_name CLUSTER BY (invoice_number);**

**Explanation**

Example:

ALTER TABLE sales\
\
CLUSTER BY (invoice_number);

This tells Delta Lake to organize future data around the specified clustering column.

After enabling clustering, you typically run:

OPTIMIZE sales;

to incrementally organize existing data according to the clustering configuration.

**YouTube**

**Enable Liquid Clustering**

https://www.youtube.com/results?search_query=Databricks+ALTER+TABLE+CLUSTER+BY

# [README](./../../../README.md)
