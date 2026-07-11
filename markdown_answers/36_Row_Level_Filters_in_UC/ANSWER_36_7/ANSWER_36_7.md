# ANSWER 36 7

**Question 7**

**Why does the lesson first implement the security logic as a dynamic view before applying a row filter to the table?**

**A. Dynamic views permanently replace the underlying table. ❌ Incorrect**

Views never replace tables.

------------------------------------------------------------------------

**B. Dynamic views execute faster than row filters. ❌ Incorrect**

The lesson is not about performance.

------------------------------------------------------------------------

**C. They allow the security logic to be validated before applying automatic enforcement at the table level. ✅ Correct**

Workflow:

Create Dynamic View

↓

Test Security Logic

↓

Verify Correct Results

↓

Attach Row Filter

Testing first reduces mistakes before enforcing security on every table query.

------------------------------------------------------------------------

**D. Row filters cannot use metadata tables directly. ❌ Incorrect**

They absolutely can.

------------------------------------------------------------------------

**E. Unity Catalog requires every row filter to be created from a view. ❌ Incorrect**

No such requirement exists.

------------------------------------------------------------------------

**Why C is correct**

Dynamic Views provide a safe way to verify security logic before enforcing it on the underlying table.

------------------------------------------------------------------------

# [README](./../../../README.md)
