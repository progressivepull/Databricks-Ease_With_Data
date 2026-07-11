# EXPLANATION 25 10

**Question 10**

**Which schema evolution mode stores unexpected columns in the \_rescued_data column without failing the stream?**

**Correct Answer**

✅ **E. rescue**

**Explanation**

Schema evolution modes include:

- addNewColumns

- failOnNewColumns

- none

- rescue

When using **rescue**:

Unexpected columns are stored inside:

\_rescued_data

as JSON instead of causing the stream to fail.

This allows ingestion to continue while preserving unexpected data for later analysis.

**Easy Memory Trick**

Unexpected Columns → \_rescued_data

**YouTube**

https://www.youtube.com/results?search_query=Databricks+rescued_data+Auto+Loader

------------------------------------------------------------------------

**Exam Cheat Sheet**

| **Question** | **Key Concept** | **Remember** |
|----|----|----|
| 1 | Purpose | Incremental cloud file ingestion |
| 2 | Technology | Structured Streaming + CloudFiles |
| 3 | Exactly Once | RocksDB in checkpoint |
| 4 | Checkpoint | Stores progress, metadata, schema, RocksDB |
| 5 | Schema Storage | cloudFiles.schemaLocation |
| 6 | Schema Hints | Override only selected columns |
| 7 | Default Detection | Directory Listing |
| 8 | Event Detection | cloudFiles.useNotifications=true |
| 9 | One-Time Processing | .trigger(availableNow=True) |
| 10 | Rescue Mode | Unexpected columns → \_rescued_data |

# [README](./../../../README.md)
