# ANSWER 26 5

**Question 5**

**What is the primary purpose of a DLT View?**

**A. To permanently store aggregated results in Unity Catalog ❌ Incorrect**

Views are not permanent storage.

Gold tables usually provide permanent curated datasets.

**B. To replace Streaming Tables in production pipelines ❌ Incorrect**

Streaming Tables and Views have different purposes.

Views perform intermediate transformations.

**C. To create temporary transformations and intermediate logic during pipeline execution ✅ Correct**

Views are useful for:

- filtering

- joining

- cleansing

- renaming columns

- intermediate calculations

Example:

Raw Orders

↓

View

(clean data)

↓

Silver Table

The View exists only during pipeline execution.

**D. To automatically optimize Delta tables ❌ Incorrect**

Optimization is handled separately.

**E. To archive historical pipeline data ❌ Incorrect**

Archiving is unrelated to DLT Views.

**Why C is correct**

Views simplify pipeline design by breaking complex transformations into reusable intermediate steps without creating permanent tables.

# [README](./../../../README.md)
