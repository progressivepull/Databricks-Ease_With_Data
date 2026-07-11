# ANSWER 27 4

**Question 4**

**Why are Streaming Tables efficient for incremental ETL?**

**A. They always reload every record from the source. ❌ Incorrect**

- Reloading everything defeats the purpose of incremental processing.

------------------------------------------------------------------------

**B. They process only new data by remembering previously processed records through checkpoints. ✅ Correct**

Streaming Tables maintain checkpoints that store:

- processed records

- stream offsets

- execution progress

This enables efficient incremental processing.

Checkpoint

↓

Already processed?

↓

Yes → Skip

No → Process

**C. They permanently cache all source data in memory. ❌ Incorrect**

- Spark memory is temporary.

- Streaming Tables rely on checkpoints, not permanent memory caching.

------------------------------------------------------------------------

**D. They require manual filtering of duplicate records. ❌ Incorrect**

- Checkpoints automatically prevent reprocessing.

- Manual duplicate filtering is generally unnecessary.

------------------------------------------------------------------------

**E. They process only CSV files. ❌ Incorrect**

Streaming Tables support many formats:

- CSV

- JSON

- Parquet

- Delta

- Auto Loader

- Kafka

------------------------------------------------------------------------

**Why B is correct**

Checkpoints enable Streaming Tables to efficiently process only new data.

------------------------------------------------------------------------

# [README](./../../../README.md)
