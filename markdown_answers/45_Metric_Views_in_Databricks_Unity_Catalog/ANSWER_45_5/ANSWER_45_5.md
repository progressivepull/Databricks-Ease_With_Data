# ANSWER 45 5

**Question 5**

**How are reusable measures referenced when querying a Metric View?**

**A. metric(total_orders)** ❌ Incorrect

- Not valid syntax.

**B. calc(total_orders)** ❌ Incorrect

- Not supported.

**C. measure(total_orders)** ✅ Correct

Example

SELECT

measure(total_orders)

FROM orders_metric_view;

The function tells Databricks:

Use the predefined measure from the Metric View.

**D. aggregate(total_orders)** ❌ Incorrect

- Not valid syntax.

**E. value(total_orders)** ❌ Incorrect

- Not supported.

**Key Concept**

Always remember:

measure(name)

------------------------------------------------------------------------

# [README](./../../../README.md)
