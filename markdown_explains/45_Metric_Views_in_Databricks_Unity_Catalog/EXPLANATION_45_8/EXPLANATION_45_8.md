# EXPLANATION 45 8

**Question 8**

**Why are joins included in Metric Views?**

**Correct Answer:**\
**C. To expose additional business dimensions, such as customer information, without requiring users to write joins themselves**

**Why C is Correct**

A Metric View can join fact tables with dimension tables.

Example:

Orders

\+

Customers

\+

Products

\+

Calendar

Business users can then filter by:

- customer

- region

- product

- salesperson

without writing SQL joins themselves.

**Why the other choices are wrong**

Joins are included to enrich the semantic model, not merely to improve performance or duplicate data.

**Memory Tip**

**Metric Views hide join complexity.**

**Individual YouTube Video**

https://www.youtube.com/watch?v=75zcOOk6How

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+Metric+Views+joins

------------------------------------------------------------------------

# [README](./../../../README.md)
