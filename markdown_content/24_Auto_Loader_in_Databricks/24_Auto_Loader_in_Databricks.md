# 24 Auto Loader in Databricks

**Auto Loader in Databricks**

Auto Loader is a Databricks feature designed to **efficiently and incrementally ingest new files** from cloud storage into Delta Lake tables. It is built on **Structured Streaming** using the **CloudFiles** source and can process data in both **streaming** and **batch** modes. Unlike COPY INTO, which is intended for repeated batch ingestion, Auto Loader continuously watches for new files and processes only those that have not been loaded before.

**Key Concepts**

**1. Purpose of Auto Loader**

- Automatically detects and loads **newly arriving files**.

- Supports:

  - Azure Data Lake Storage (ADLS)

  - Amazon S3

  - Google Cloud Storage (GCS)

  - DBFS

  - Unity Catalog Volumes

- Designed for large-scale ingestion (millions of files per hour).

------------------------------------------------------------------------

**2. Incremental Processing**

Auto Loader guarantees **exactly-once processing**:

- Previously processed files are never loaded again.

- Only new files are processed.

- Metadata about processed files is stored in the checkpoint directory using **RocksDB**.

------------------------------------------------------------------------

**3. CloudFiles Source**

Auto Loader uses the Structured Streaming source named **CloudFiles**.

Typical read pattern:

spark.readStream \\\
.format("cloudFiles") \\\
.option("cloudFiles.format","csv")

Benefits:

- Uses familiar Structured Streaming APIs.

- Can write to Delta tables using writeStream.

------------------------------------------------------------------------

**4. Checkpoint Location**

A checkpoint directory stores:

- Progress information

- Processed file metadata

- RocksDB database

- Schema information

Without checkpoints:

- Auto Loader cannot track processed files.

- Exactly-once processing is lost.

------------------------------------------------------------------------

**5. Schema Location**

Auto Loader stores inferred schemas separately.

.option("cloudFiles.schemaLocation", checkpointPath)

This enables:

- Schema inference

- Schema evolution

- Automatic schema updates

------------------------------------------------------------------------

**6. Schema Hints**

Instead of defining the full schema, you can override only selected columns.

Example:

.option(\
"cloudFiles.schemaHints",\
"quantity INT, unit_price DOUBLE"\
)

Advantages:

- Less typing

- More flexible than supplying a full schema

- Remaining columns are inferred automatically.

------------------------------------------------------------------------

**File Detection Modes**

Auto Loader detects new files using two methods.

**A. Directory Listing (Default)**

- Periodically scans cloud storage directories.

- Uses storage API calls.

- Stores metadata in RocksDB.

Advantages:

- No special cloud permissions required.

- Works immediately.

Disadvantages:

- Slightly slower for very large environments.

------------------------------------------------------------------------

**B. File Notification**

Instead of scanning directories:

- Uses cloud notification services.

- Receives events whenever files arrive.

- Uses queues such as:

  - Azure Event Grid

  - AWS SQS

  - Google Pub/Sub

Enable with:

.option("cloudFiles.useNotifications","true")

Advantages:

- Faster

- More scalable

- Less directory scanning

Requires elevated cloud permissions to create notification infrastructure.

------------------------------------------------------------------------

**Writing Data**

Typical write operation:

df.writeStream \\\
.option("checkpointLocation", checkpointPath) \\\
.outputMode("append") \\\
.trigger(availableNow=True) \\\
.toTable("sales")

Important options:

- checkpointLocation

- outputMode("append")

- trigger(availableNow=True) for batch processing

- toTable() to write directly to Delta tables

------------------------------------------------------------------------

**Batch vs Streaming**

**Batch Mode**

.trigger(availableNow=True)

Processes:

- All currently available files.

- Stops automatically.

Useful for scheduled jobs.

**Streaming Mode**

.trigger(processingTime="30 seconds")

Runs continuously and checks for new files periodically.

------------------------------------------------------------------------

**Schema Evolution**

Auto Loader can automatically adapt when incoming files contain new columns.

Four schema evolution modes are available.

------------------------------------------------------------------------

**1. addNewColumns (Default)**

Behavior:

- Detects new columns.

- Updates stored schema.

- First run fails with an UnknownFieldException.

- After schema update, rerunning succeeds.

Use when:

- You want your Delta table to grow as new columns appear.

Also requires:

.option("mergeSchema","true")

when writing to Delta tables.

------------------------------------------------------------------------

**2. rescue**

.option(\
"cloudFiles.schemaEvolutionMode",\
"rescue"\
)

Behavior:

- Stream never fails.

- Unknown columns are stored in a special \_rescued_data column.

Advantages:

- No interruption.

- Preserve unexpected data for later processing.

------------------------------------------------------------------------

**3. none**

.option(\
"cloudFiles.schemaEvolutionMode",\
"none"\
)

Behavior:

- Unknown columns are ignored.

- No rescued data.

- Stream continues normally.

Useful when:

- Extra columns are unimportant.

- You want a stable schema.

------------------------------------------------------------------------

**4. failOnNewColumns**

Behavior:

- Stream immediately fails whenever a new column appears.

- Requires manual schema changes before processing can continue.

Useful in environments with strict schema control.

------------------------------------------------------------------------

**Nested Folder Support**

Auto Loader easily reads hierarchical folder structures such as:

landing/\
2025/\
01/\
01/\
02/\
03/

Using wildcards:

.load("/landing/\*/\*/\*")

It automatically discovers files within nested directories.

------------------------------------------------------------------------

**Metadata Columns**

Auto Loader exposes useful metadata, including:

\_metadata.file_name

This allows tracking:

- Source filename

- Origin of each record

- Auditing and troubleshooting.

------------------------------------------------------------------------

**RocksDB**

Checkpoint folders contain a **RocksDB** database.

Purpose:

- Tracks processed files.

- Enables exactly-once processing.

- Scales to millions of files efficiently.

------------------------------------------------------------------------

**Auto Loader vs COPY INTO**

| **Feature**                   | **COPY INTO** | **Auto Loader** |
|-------------------------------|---------------|-----------------|
| Incremental loading           | Yes           | Yes             |
| Continuous ingestion          | No            | Yes             |
| Built on Structured Streaming | No            | Yes             |
| Exactly-once processing       | Yes           | Yes             |
| Handles schema evolution      | Limited       | Extensive       |
| Supports streaming            | No            | Yes             |
| Large-scale file ingestion    | Good          | Excellent       |
| File notifications            | No            | Yes             |

------------------------------------------------------------------------

**Key Exam Takeaways**

- **Auto Loader** incrementally ingests new files into Delta tables.

- Built on **Structured Streaming** using the **CloudFiles** source.

- Supports **Azure, AWS, GCP, DBFS, and Unity Catalog Volumes**.

- Uses **checkpoints** and **RocksDB** for exactly-once processing.

- Can run in **batch** (availableNow) or **streaming** mode.

- Supports **schema inference**, **schema hints**, and **schema evolution**.

- Four schema evolution modes:

  - addNewColumns (default)

  - rescue

  - none

  - failOnNewColumns

- Supports **directory listing** (default) and **file notification** detection modes.

- cloudFiles.useNotifications=true enables event-based file detection.

- mergeSchema=true is required when adding new columns to Delta tables.

- \_rescued_data stores unexpected columns when using **rescue** mode.

# [README](./../../../README.md)
