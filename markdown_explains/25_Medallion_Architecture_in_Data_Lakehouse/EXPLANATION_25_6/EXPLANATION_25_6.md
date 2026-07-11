# EXPLANATION 25 6

**Question 6**

**Which statement correctly describes Schema Hints?**

**Correct Answer**

✅ **C. Only selected columns are overridden while the remaining columns are inferred automatically.**

**Explanation**

Schema hints let you manually define only certain columns.

Example:

Without hints:

id

name

salary

Auto Loader infers all three.

With hints:

salary DOUBLE

Now:

- salary becomes DOUBLE

- everything else is still inferred automatically

This is useful when Auto Loader guesses the wrong data type for a few columns.

**Easy Memory Trick**

Hints = Override only what you want.

**YouTube**

https://www.youtube.com/results?search_query=Databricks+Auto+Loader+Schema+Hints

------------------------------------------------------------------------

# [README](./../../../README.md)
