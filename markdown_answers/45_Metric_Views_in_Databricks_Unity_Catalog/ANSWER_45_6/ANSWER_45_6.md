# ANSWER 45 6

**Question 6**

**Which SQL statement is not supported when querying a Metric View?**

**A. SELECT measure(total_orders) FROM orders_metric_view** ❌ Incorrect

- Valid.

**B. SELECT order_status_readable, measure(total_orders) GROUP BY order_status_readable** ❌ Incorrect

- Valid.

**C. SELECT \* FROM orders_metric_view** ✅ Correct

Why?

Metric Views aren't normal tables.

They expose:

- Measures

- Dimensions

You must explicitly request them.

Instead use:

SELECT

measure(total_orders)

or

SELECT

order_year,

measure(total_orders)

**D. SELECT measure(total_price) FROM orders_metric_view** ❌ Incorrect

- Valid if defined.

**E. SELECT order_year, measure(total_orders) GROUP BY order_year** ❌ Incorrect

- Valid.

**Key Concept**

**Metric Views do NOT support SELECT \*.**

------------------------------------------------------------------------

# [README](./../../../README.md)
