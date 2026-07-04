# EXPLANATION 14 7

**Question 7**

**Which statement best describes CTAS (Create Table As Select)?**

**Correct Answer:**\
✅ **It creates a new table with copied data but may not preserve all Delta metadata.**

**Explanation**

CTAS means:

**Create Table As Select**

Example:

CREATE TABLE sales_copy AS\
\
SELECT \*\
\
FROM sales;

What CTAS copies:

✅ Data

What CTAS may **not** preserve:

- Table properties

- Comments

- Constraints

- Some metadata

- Delta-specific settings

It is ideal for quickly creating a new table populated with query results.

**YouTube**

**CTAS in Databricks**

https://www.youtube.com/results?search_query=Databricks+CTAS

# [README](./../../../README.md)
