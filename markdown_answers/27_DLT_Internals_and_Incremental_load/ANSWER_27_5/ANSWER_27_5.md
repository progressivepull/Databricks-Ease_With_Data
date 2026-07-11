# ANSWER 27 5

**Question 5**

**What happens to Materialized Views when upstream data changes?**

**A. They must be manually refreshed by the developer. ❌ Incorrect**

- DLT automatically refreshes Materialized Views.

------------------------------------------------------------------------

**B. They become read-only until rebuilt. ❌ Incorrect**

- Materialized Views remain usable and continue updating.

------------------------------------------------------------------------

**C. They automatically recompute joins and aggregations to produce the latest results. ✅ Correct**

Example:

Bronze

↓

Silver

↓

Materialized View

If Silver changes:

Silver updated

↓

Materialized View recomputes

↓

Latest results available

No manual intervention is required.

------------------------------------------------------------------------

**D. They stop accepting new data until the schema is recreated. ❌ Incorrect**

- Schema changes are handled automatically by DLT when supported.

------------------------------------------------------------------------

**E. They are converted into temporary views. ❌ Incorrect**

- Materialized Views remain Materialized Views.

------------------------------------------------------------------------

**Why C is correct**

Materialized Views automatically recompute their results whenever upstream data changes.

------------------------------------------------------------------------

# [README](./../../../README.md)
