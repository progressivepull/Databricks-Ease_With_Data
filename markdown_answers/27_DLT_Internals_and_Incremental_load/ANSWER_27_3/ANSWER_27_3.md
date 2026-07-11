# ANSWER 27 3

**Question 3**

**When 10,000 new rows are added to the orders_raw table and the DLT pipeline is rerun, what happens?**

**A. The entire Orders and Customers datasets are reprocessed. ❌ Incorrect**

- Streaming Tables are incremental.

- Reprocessing everything would waste time and resources.

------------------------------------------------------------------------

**B. Only the Customers Bronze table is refreshed. ❌ Incorrect**

- The new data was added to orders_raw, not customers.

- Refreshing only customers would ignore the new order records.

------------------------------------------------------------------------

**C. Only the new 10,000 order records are processed by the Streaming Table, and downstream layers are updated automatically. ✅ Correct**

Streaming Tables remember previously processed data using checkpoints.

Workflow:

Old Data

100,000 rows

New Data

10,000 rows

Pipeline Run

↓

Process only

10,000 new rows

↓

Automatically update

Silver

↓

Automatically update

Gold

Only new data is processed.

------------------------------------------------------------------------

**D. The Gold table must be rebuilt manually. ❌ Incorrect**

- DLT automatically updates downstream datasets.

- Manual rebuilding is unnecessary.

------------------------------------------------------------------------

**E. All checkpoints are deleted before processing begins. ❌ Incorrect**

- Deleting checkpoints would force a full reprocessing.

- DLT keeps checkpoints specifically to avoid this.

------------------------------------------------------------------------

**Why C is correct**

DLT processes only newly arrived data and automatically propagates changes through downstream datasets.

------------------------------------------------------------------------

# [README](./../../../README.md)
