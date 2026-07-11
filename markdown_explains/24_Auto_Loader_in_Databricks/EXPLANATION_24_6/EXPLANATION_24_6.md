# EXPLANATION 24 6

**Question 6**

**Which statement correctly describes Schema Hints in Auto Loader?**

**Correct Answer:** **C. Only selected columns are overridden while the remaining columns are inferred automatically.**

**Explanation**

Schema Hints allow you to override only the columns you know should have a different data type.

Example:

Without hint:

CustomerID → STRING

Schema Hint:

CustomerID → INT

Everything else continues to be inferred automatically. This gives you fine-grained control without requiring a complete schema definition.

**YouTube**

- https://www.youtube.com/results?search_query=Databricks+Schema+Hints+Auto+Loader

- https://www.youtube.com/results?search_query=Auto+Loader+schema+evolution

------------------------------------------------------------------------

# [README](./../../../README.md)
