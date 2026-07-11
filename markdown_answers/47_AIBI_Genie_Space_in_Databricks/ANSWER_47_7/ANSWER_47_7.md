# ANSWER 47 7

**Question 7**

**What does the Show Code option allow users to do?**

**A. Modify the SQL Warehouse configuration** ❌ Incorrect

- Warehouse settings aren't editable here.

**B. Create new datasets for Genie** ❌ Incorrect

- Datasets are managed separately.

**C. Inspect the generated SQL, including filters, joins, and aggregations** ✅ Correct

This is extremely useful.

You can see exactly what Genie generated.

Example

SELECT

SUM(sales)

FROM orders

WHERE year = 2025

GROUP BY region;

You can verify:

- Filters

- Joins

- GROUP BY

- Aggregations

This builds trust in the AI.

**D. Change Unity Catalog metadata directly** ❌ Incorrect

- Metadata editing happens elsewhere.

**E. Edit dashboard permissions** ❌ Incorrect

- Permissions aren't changed through Show Code.

**Key Concept**

**Show Code = Transparency into the generated SQL.**

# [README](./../../../README.md)
