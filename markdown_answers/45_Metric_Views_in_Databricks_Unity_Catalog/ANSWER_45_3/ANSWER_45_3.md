# ANSWER 45 3

**Question 3**

**How are Metric Views created in Databricks?**

**A. Using Python notebooks only** ❌ Incorrect

- Python can query Metric Views.

- It doesn't define them.

**B. Using SQL stored procedures** ❌ Incorrect

- Metric Views aren't stored procedures.

**C. Using YAML definitions** ✅ Correct

Metric Views are defined using YAML.

Why?

Because YAML is:

- Easy to version control

- Easy to review

- Easy to reuse

- Human readable

Example

dimensions:

order_year

measures:

total_orders

**D. Using JSON configuration files** ❌ Incorrect

- JSON isn't used for Metric View definitions.

**E. Using Scala classes** ❌ Incorrect

- Scala is unrelated here.

**Key Concept**

**Metric Views are Infrastructure-as-Code using YAML.**

------------------------------------------------------------------------

# [README](./../../../README.md)
