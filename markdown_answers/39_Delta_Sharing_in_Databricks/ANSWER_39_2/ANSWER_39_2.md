# ANSWER 39 2

**Question 2**

**Which operation can a Delta Sharing recipient perform on shared data?**

**A. Insert new rows into shared tables ❌ Incorrect**

Recipients have **read-only** access.

They cannot:

- INSERT

- UPDATE

- DELETE

**B. Update existing records in shared tables ❌ Incorrect**

Only the provider controls the underlying data.

**C. Delete shared data from the provider's environment ❌ Incorrect**

Recipients never control the provider's data.

**D. Query and read shared objects without modifying them ✅ Correct**

Recipients can perform queries such as:

SELECT \*

FROM shared_catalog.sales.orders;

They can:

- filter

- aggregate

- join

- analyze

But cannot modify the provider's data.

**E. Rename shared tables in the provider's catalog ❌ Incorrect**

Only the provider manages shared objects.

**Why D is correct**

Delta Sharing is intentionally **read-only**, protecting the provider's data while allowing recipients to analyze it.

# [README](./../../../README.md)
