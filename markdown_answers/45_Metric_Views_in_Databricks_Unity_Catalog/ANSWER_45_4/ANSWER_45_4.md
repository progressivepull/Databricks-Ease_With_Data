# ANSWER 45 4

**Question 4**

**What is the primary benefit of defining business logic once in a Metric View?**

**A. It automatically creates dashboards for every user.** ❌ Incorrect

- Users still build dashboards.

**B. It ensures everyone uses the same KPI calculations and reduces duplicated SQL.** ✅ Correct

Without Metric Views

Every dashboard contains:

SUM(price)

or

SUM(price \* quantity)

Different developers may write different formulas.

With Metric Views

Everyone simply writes:

measure(total_sales)

The calculation exists once.

Benefits:

- Consistent KPIs

- Less SQL duplication

- Easier maintenance

**C. It eliminates the need for Unity Catalog.** ❌ Incorrect

- Metric Views are stored **inside Unity Catalog**.

**D. It converts all data into Delta format.** ❌ Incorrect

- Metric Views don't transform storage.

**E. It replaces SQL with Python for analytics.** ❌ Incorrect

- SQL is still used.

**Key Concept**

**Define once → Reuse everywhere**

------------------------------------------------------------------------

# [README](./../../../README.md)
