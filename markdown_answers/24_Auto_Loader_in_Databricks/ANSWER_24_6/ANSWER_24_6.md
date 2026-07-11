# ANSWER 24 6

**Question 6**

**Which statement correctly describes Schema Hints in Auto Loader?**

**A. Every column must be explicitly defined.** ❌ Incorrect

Only columns you want to override need hints.

------------------------------------------------------------------------

**B. Schema hints completely disable schema inference.** ❌ Incorrect

Inference still happens.

Hints only modify selected columns.

------------------------------------------------------------------------

**C. Only selected columns are overridden while the remaining columns are inferred automatically.** ✅ Correct

Example:

CustomerID -\> STRING

Everything else is inferred automatically.

------------------------------------------------------------------------

**D. Schema hints are supported only for JSON files.** ❌ Incorrect

They work with multiple supported file formats.

------------------------------------------------------------------------

**E. Schema hints prevent schema evolution entirely.** ❌ Incorrect

Schema evolution still works.

Hints simply override specified columns.

------------------------------------------------------------------------

**Why C is correct**

Schema hints are partial schema overrides.

------------------------------------------------------------------------

# [README](./../../../README.md)
