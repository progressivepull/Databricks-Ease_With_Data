# ANSWER 42 9

**Question 9**

**What optimization does Databricks perform when a Materialized View refresh detects no new data?**

**A. It automatically performs a full table recomputation.** ❌ Incorrect

- That would waste resources.

**B. It deletes all cached results.** ❌ Incorrect

- Cached results remain valid.

**C. It performs a No Operation (NO OP), skipping unnecessary processing.** ✅ Correct

- If no data changed:

  - Nothing is recomputed.

  - Existing results remain.

  - Compute resources are saved.

**D. It rebuilds the DLT pipeline from scratch.** ❌ Incorrect

- DLT doesn't rebuild unless necessary.

**E. It converts the Materialized View into a Streaming Table.** ❌ Incorrect

- These are separate object types.

**Key Concept**

**No data changed → NO OP → No unnecessary work.**

# [README](./../../../README.md)
