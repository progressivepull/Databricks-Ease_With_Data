# 25 Medallion Architecture in Data Lakehouse

**Databricks Auto Loader**

This lesson introduces **Databricks Auto Loader**, a scalable file ingestion utility designed to incrementally process new files arriving in cloud storage. Built on **Structured Streaming** using the **CloudFiles** source, Auto Loader efficiently detects, tracks, and ingests files into Delta tables while supporting schema evolution and exactly-once processing.

**1. What is Auto Loader?**

Auto Loader is a Databricks feature used to **incrementally ingest files** from cloud storage into Delta Lake.

Supported storage includes:

- Azure Data Lake Storage (ADLS)

- Amazon S3

- Google Cloud Storage (GCS)

- Databricks Volumes

- DBFS

Instead of repeatedly scanning and loading every file, Auto Loader detects **only new files** and processes them once.

**2. Built on Structured Streaming**

Auto Loader uses the **CloudFiles** Structured Streaming source.

Reading data looks very similar to Structured Streaming:

spark.readStream \\\
.format("cloudFiles")

Because it uses Structured Streaming, Auto Loader supports:

- Streaming ingestion

- Batch-style ingestion

- Incremental processing

- Checkpointing

**3. Benefits of Auto Loader**

Auto Loader provides:

- Incremental file ingestion

- Exactly-once processing

- Automatic schema management

- Massive scalability (millions of files/hour)

- Nested directory support

- Integration with Delta Lake

Compared with COPY INTO, Auto Loader is designed for **continuous ingestion of newly arriving files** rather than repeatedly running batch loads.

**4. Reading Files**

The lesson demonstrates reading CSV files from a nested folder structure.

Example directory:

landing/\
2024/\
01/\
01/\
invoice1.csv\
02/\
invoice2.csv\
03/\
invoice3.csv

Using wildcards allows Auto Loader to recursively discover files in nested folders.

**5. Basic Auto Loader Example**

Typical configuration:

spark.readStream\
.format("cloudFiles")\
.option("cloudFiles.format","csv")\
.load(path)

Important options include:

- file format

- schema location

- header

- path filters

These configure how Auto Loader reads and tracks files.

**6. Path Filtering**

The lesson uses:

.option("pathGlobFilter","\*.csv")

This tells Auto Loader to process only CSV files while ignoring other file types in the same directory.

**7. Schema Location**

One of the most important settings is:

cloudFiles.schemaLocation

This directory stores:

- Inferred schema

- Updated schemas

- Schema evolution metadata

Auto Loader uses this location whenever file schemas change.

**8. Schema Hints**

Instead of defining an entire schema, Auto Loader supports **Schema Hints**.

Example:

- Quantity → Integer

- Unit Price → Double

Benefits:

- Only specify important columns.

- Let Auto Loader infer the remaining columns.

- Less code to maintain.

**9. Writing Data**

The lesson writes data using Structured Streaming.

Important options:

- Checkpoint Location

- Append Mode

- Trigger

- Delta Table

The destination table receives only newly detected files.

**10. Available Now Trigger**

Instead of running continuously, the lesson uses the **Available Now** trigger.

Behavior:

Read all available files\
\
↓\
\
Process them\
\
↓\
\
Stop automatically

This allows Auto Loader to behave like a batch job while still using Structured Streaming internally.

**11. Exactly-Once Processing**

The lesson reruns the ingestion after processing the initial files.

Result:

- No duplicate records

- Previously processed files are skipped

This demonstrates Auto Loader's **exactly-once semantics**, preventing duplicate ingestion.

**12. Incremental File Detection**

After adding a fifth CSV file:

Day 1\
Day 2\
Day 3\
\
↓\
\
Run\
\
↓\
\
Files processed

Later:

Add Day 5\
\
↓\
\
Run Again\
\
↓\
\
Only Day 5 processed

Existing files are ignored because Auto Loader remembers which files have already been ingested.

**13. File Detection Modes**

Auto Loader supports two methods for detecting new files.

**Directory Listing (Default)**

Uses cloud storage APIs to scan directories for new files.

Characteristics:

- No special cloud permissions

- Works everywhere

- Tracks processed files using RocksDB

**File Notification**

Uses:

- Cloud notification service

- Queue service

Workflow:

New File\
\
↓\
\
Cloud Notification\
\
↓\
\
Queue\
\
↓\
\
Auto Loader

Advantages:

- Faster detection

- More scalable

Requirements:

- Elevated cloud permissions

- Cloud resources created automatically

**14. Checkpoints**

Auto Loader stores checkpoint information.

Checkpoint contents include:

- Processed files

- Streaming offsets

- Metadata

This enables:

- Exactly-once ingestion

- Restart recovery

- Incremental processing

**15. RocksDB**

Inside the checkpoint directory, Auto Loader uses **RocksDB**.

Purpose:

- Tracks processed files

- Scales to millions of files

- Prevents duplicate ingestion

RocksDB is one of the core technologies behind Auto Loader's scalability.

**16. Schema Evolution**

Real-world files often change over time.

Example:

Original file:

Invoice\
Customer\
Quantity\
Price

Later:

Invoice\
Customer\
Quantity\
Price\
State

Auto Loader supports multiple strategies for handling these schema changes.

**17. Schema Evolution Modes**

Auto Loader supports four modes.

**A. Add New Columns (Default)**

Behavior:

- Detects new columns

- Updates schema

- Requires rerunning the stream

- Can merge schema into the Delta table

This is the default behavior when no schema evolution mode is specified.

**B. Rescue**

Behavior:

- Stream continues

- New columns are stored in a special **rescued data** column

- Existing schema remains unchanged

Useful when you don't want ingestion to stop because of unexpected columns.

**C. None**

Behavior:

- Ignore new columns

- No rescued data

- Stream continues

- Unexpected fields are discarded

This is appropriate when extra columns are not important.

**D. Fail on New Columns**

Behavior:

- Stream stops immediately when new columns appear

- Requires manual schema updates before processing can continue

Useful in environments with strict schema control.

**18. Merge Schema**

When using **Add New Columns**, the Delta table must also allow schema updates.

Enabling schema merge lets new columns be added to the destination table automatically during ingestion.

**19. Hidden Metadata Columns**

The lesson demonstrates adding the source filename to each record using the hidden metadata column:

\_metadata.file_name

This allows users to identify which file produced each row, which is useful for auditing and troubleshooting.

**20. Internal Architecture**

Auto Loader maintains two key internal directories:

Checkpoint\
│\
├── RocksDB\
│\
└── Metadata

and

Schema Location\
│\
└── \_schemas

These internal structures enable reliable incremental processing and schema evolution.

**21. Switching to File Notification Mode**

To use the notification-based detection mechanism, Auto Loader can be configured to use cloud notifications instead of directory listing.

When enabled:

- Cloud storage publishes notifications for new files.

- Notifications are placed in a queue.

- Auto Loader consumes the queue to discover new files without scanning directories.

This mode offers faster detection but requires additional cloud permissions and setup.

**Key Takeaways**

- **Auto Loader** is Databricks' scalable solution for continuously ingesting new files from cloud storage into Delta Lake.

- It is built on **Structured Streaming** using the **CloudFiles** source, allowing both streaming and batch-style ingestion.

- Auto Loader guarantees **exactly-once processing** through **checkpointing** and **RocksDB**, ensuring files are never processed twice.

- It supports **incremental ingestion**, processing only newly arrived files while skipping previously ingested ones.

- Auto Loader provides flexible **schema evolution** with four modes: **Add New Columns**, **Rescue**, **None**, and **Fail on New Columns**.

- **Schema Hints** simplify type assignment without requiring a full schema definition.

- Two file detection methods are available:

  - **Directory Listing** (default), which scans cloud storage.

  - **File Notification**, which uses cloud-native event and queue services for faster, more scalable detection.

- Internal **schema** and **checkpoint** directories maintain metadata that allows Auto Loader to recover from failures, evolve schemas, and scale efficiently to millions of files.

# [README](./../../../README.md)
