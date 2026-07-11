# ANSWER 27 7

**Question 7**

**What happens when a dataset such as joined_silver is renamed to order_silver in the DLT notebook?**

**A. Both datasets remain in Unity Catalog permanently. ❌ Incorrect**

- Leaving both datasets would create duplicate pipeline outputs.

------------------------------------------------------------------------

**B. Developers must manually delete the old dataset after the pipeline completes. ❌ Incorrect**

- DLT manages obsolete datasets automatically.

------------------------------------------------------------------------

**C. DLT automatically removes the old dataset, creates the new one, and updates pipeline metadata. ✅ Correct**

Pipeline change:

Before:

joined_silver

After:

order_silver

DLT automatically:

- removes obsolete dataset

- creates new dataset

- updates dependencies

- updates metadata

------------------------------------------------------------------------

**D. The pipeline fails because dataset names cannot be changed. ❌ Incorrect**

- Dataset names can be changed.

------------------------------------------------------------------------

**E. Only the notebook name changes; the dataset name remains the same. ❌ Incorrect**

- Dataset names come from pipeline definitions, not notebook filenames.

------------------------------------------------------------------------

**Why C is correct**

DLT automatically synchronizes dataset definitions with the current pipeline code.

------------------------------------------------------------------------

# [README](./../../../README.md)
