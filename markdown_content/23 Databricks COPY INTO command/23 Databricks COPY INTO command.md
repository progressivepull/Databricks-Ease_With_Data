# 23 Databricks COPY INTO command

**Databricks COPY INTO Command**

This lesson introduces the **COPY INTO** SQL command, a simple and powerful ingestion utility for loading files into Delta tables. It highlights COPY INTO's support for multiple file formats, **exactly-once processing**, **idempotent behavior**, **schema inference**, **schema evolution**, and incremental loading.

------------------------------------------------------------------------

**Key Topics Covered**

**1. What is COPY INTO?**

COPY INTO is a SQL command used to ingest files from cloud storage or Unity Catalog volumes into Delta tables.

It supports multiple source formats, including:

- CSV

- JSON

- Parquet

- Avro

- Text

- Binary files

COPY INTO is designed for **batch ingestion** scenarios.

------------------------------------------------------------------------

**2. Key Features**

COPY INTO provides several important capabilities:

- Exactly-once ingestion

- Retryable execution

- Idempotent behavior

- Schema inference

- Schema evolution

- Incremental loading

These features make it ideal for reliable batch pipelines.

------------------------------------------------------------------------

**3. What Does Idempotent Mean?**

An operation is **idempotent** if running it multiple times produces the same final result.

For COPY INTO:

- A file is loaded only once.

- Re-running the same command does not duplicate data.

- Previously processed files are skipped automatically.

This enables safe retries without creating duplicate records.

------------------------------------------------------------------------

**4. Preparing the Landing Area**

The lesson first creates:

- A managed Unity Catalog volume

- An **Input** folder inside the volume

This folder acts as the landing zone for incoming data files.

Example structure:

Volumes\
└── dev\
└── branch\
└── landing\
└── input

------------------------------------------------------------------------

**5. Copying Source Files**

Using **DBUtils**, two CSV files are copied into the landing folder.

These invoice files become the source for the COPY INTO operation.

------------------------------------------------------------------------

**6. Creating a Placeholder Table**

Instead of defining columns manually, the lesson creates an empty Delta table:

CREATE TABLE dev.branch.invoice_cp;

Characteristics:

- No schema defined

- No columns

- Serves as a placeholder

The schema will be inferred during ingestion.

------------------------------------------------------------------------

**7. Using COPY INTO**

The COPY INTO command specifies:

- Target Delta table

- Source folder

- File format

- File pattern

- Source options

- Target options

Source configuration includes:

- CSV format

- Header row

- Schema merging

Target configuration enables:

- Schema evolution

During execution:

- Columns are automatically created.

- Data is loaded into the Delta table.

------------------------------------------------------------------------

**8. Schema Inference**

Since the table contains no predefined schema:

COPY INTO automatically:

- Detects column names

- Detects data types

- Creates the Delta table schema

This eliminates manual schema creation.

------------------------------------------------------------------------

**9. Viewing the Loaded Data**

After execution:

SELECT \*\
FROM dev.branch.invoice_cp;

confirms that both CSV files have been successfully ingested.

------------------------------------------------------------------------

**10. Demonstrating Idempotency**

The instructor immediately reruns the same COPY INTO command.

Result:

- No new rows inserted

- No files processed

COPY INTO recognizes that the files have already been loaded.

This demonstrates its **exactly-once** behavior.

------------------------------------------------------------------------

**11. How COPY INTO Tracks Processed Files**

The lesson examines the Delta table storage location.

Inside the Delta transaction log (\_delta_log), COPY INTO maintains metadata that records previously processed files.

Because of this metadata:

- Previously loaded files are skipped.

- Duplicate ingestion is prevented.

------------------------------------------------------------------------

**12. Custom Schema Example**

Next, the lesson creates a second table with a predefined schema.

Columns include:

- Invoice Number

- Stock Code

- Quantity

- Insert Date

Unlike the placeholder table, this table already has defined column types.

------------------------------------------------------------------------

**13. Transforming Data During Load**

Instead of loading raw files directly, COPY INTO wraps the source with a SELECT statement.

The SELECT performs transformations such as:

- Selecting specific columns

- Casting data types

- Creating new columns

Example transformation:

- Cast Quantity to DOUBLE

- Add:

CURRENT_TIMESTAMP

as an **Insert Date**

This allows basic ETL transformations during ingestion.

------------------------------------------------------------------------

**14. Loading Additional Files**

A third CSV file is copied into the landing folder.

Running COPY INTO again processes only:

- The new file

Previously processed files remain skipped.

This demonstrates incremental ingestion.

------------------------------------------------------------------------

**15. Incremental Processing**

COPY INTO automatically detects:

- New files

- Previously processed files

Only new files are loaded.

This greatly simplifies recurring batch ingestion pipelines.

------------------------------------------------------------------------

**COPY INTO Workflow**

Landing Folder\
│\
▼\
COPY INTO\
│\
├── Previously Processed?\
│\
├── Yes ─────► Skip\
│\
└── No ─────► Load\
│\
▼\
Delta Table

------------------------------------------------------------------------

**Placeholder Table vs Predefined Schema**

| **Placeholder Table**         | **Predefined Table**              |
|-------------------------------|-----------------------------------|
| No schema                     | Schema already exists             |
| Schema inferred automatically | Uses existing schema              |
| Requires schema merge         | Does not require schema inference |
| Best for unknown structures   | Best for controlled data models   |

------------------------------------------------------------------------

**COPY INTO Features**

| **Feature**         | **Supported** |
|---------------------|---------------|
| CSV                 | ✔             |
| JSON                | ✔             |
| Parquet             | ✔             |
| Avro                | ✔             |
| Binary Files        | ✔             |
| Schema Inference    | ✔             |
| Schema Evolution    | ✔             |
| Exactly Once        | ✔             |
| Incremental Loading | ✔             |

------------------------------------------------------------------------

**COPY INTO vs Auto Loader**

The instructor concludes by explaining when COPY INTO should be used.

**COPY INTO**

Best for:

- Small to medium batch ingestion

- Hundreds or thousands of files

- Periodic loads

- Simple pipelines

------------------------------------------------------------------------

**Auto Loader**

Recommended when:

- Millions of files arrive continuously

- Complex directory structures exist

- Streaming ingestion is required

- Large-scale production pipelines are needed

Auto Loader will be introduced in the next lesson.

------------------------------------------------------------------------

**Key Takeaways**

- **COPY INTO** is a SQL-based ingestion utility that loads files into Delta tables while supporting multiple source formats such as CSV, JSON, Parquet, and Avro.

- It provides **exactly-once** and **idempotent** processing, ensuring that previously ingested files are automatically skipped even if the command is executed multiple times.

- COPY INTO supports **schema inference** and **schema evolution**, allowing data to be loaded into placeholder tables without manually defining the schema.

- Source data can be transformed during ingestion using a **SELECT** statement, enabling operations such as column selection, data type casting, and adding computed columns like timestamps.

- COPY INTO maintains ingestion metadata within the Delta transaction log (\_delta_log) to track processed files and support incremental loading.

- When new files are added to the landing location, COPY INTO processes only those new files while ignoring previously loaded ones.

- COPY INTO is well suited for **batch ingestion workloads**, while **Auto Loader** is the preferred solution for large-scale, continuously arriving datasets with millions of files.

# [README](./../../../README.md)
