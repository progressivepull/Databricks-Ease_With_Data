# ANSWER 26 6

**Question 6**

**Which keyword is used to reference datasets created earlier within the same Delta Live Tables pipeline?**

**A. CURRENT ❌ Incorrect**

Not a DLT keyword.

**B. DELTA ❌ Incorrect**

Delta refers to Delta Lake.

Not internal pipeline references.

**C. LIVE ✅ Correct**

Example:

SELECT \*

FROM LIVE.customers

LIVE references datasets already created within the current DLT pipeline.

**D. PIPELINE ❌ Incorrect**

Not valid syntax.

**E. STREAM ❌ Incorrect**

STREAM is used for reading streaming sources, not referencing previous DLT datasets.

**Why C is correct**

LIVE allows DLT datasets within the same pipeline to reference one another cleanly and automatically.

# [README](./../../../README.md)
