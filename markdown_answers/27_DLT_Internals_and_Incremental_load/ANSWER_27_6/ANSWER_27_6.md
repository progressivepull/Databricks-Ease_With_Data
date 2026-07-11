# ANSWER 27 6

**Question 6**

**How does Delta Live Tables handle schema evolution when a developer renames a column or adds a new aggregation?**

**A. The developer must manually alter the destination table before running the pipeline. ❌ Incorrect**

- Traditional ETL may require manual schema changes.

- DLT automates schema updates.

------------------------------------------------------------------------

**B. The schema cannot be changed after the pipeline is created. ❌ Incorrect**

- DLT supports schema evolution.

------------------------------------------------------------------------

**C. Only the transformation code needs to be updated, and DLT automatically applies the schema changes during execution. ✅ Correct**

Example:

Original:

select("customer_id")

Updated:

select("customer_identifier")

DLT detects the change and updates the destination schema.

------------------------------------------------------------------------

**D. The existing pipeline must be deleted and recreated. ❌ Incorrect**

- Pipelines can evolve without recreation.

------------------------------------------------------------------------

**E. Schema changes are supported only for Streaming Tables. ❌ Incorrect**

- Schema evolution is not limited to Streaming Tables.

------------------------------------------------------------------------

**Why C is correct**

Developers update transformation logic, and DLT applies the corresponding schema changes automatically.

------------------------------------------------------------------------

# [README](./../../../README.md)
