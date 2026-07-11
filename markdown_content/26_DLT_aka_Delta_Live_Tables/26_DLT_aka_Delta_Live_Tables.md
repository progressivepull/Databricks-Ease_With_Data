# 26 DLT aka Delta Live Tables

**Databricks Delta Live Tables (DLT) Introduction**

This lesson introduces **Delta Live Tables (DLT)**, a declarative ETL framework in Databricks that simplifies building, managing, and monitoring data pipelines. Instead of manually managing clusters, orchestration, retries, and data quality, developers only define the transformations, while DLT handles the operational aspects automatically.

**What is Delta Live Tables (DLT)?**

Delta Live Tables is a **declarative data pipeline framework** built on **Delta Lake**.

With DLT, developers focus only on:

- Reading data

- Transforming data

- Writing business logic

DLT automatically manages:

- Pipeline orchestration

- Cluster management

- Dependency tracking

- Error handling

- Pipeline execution

- Data quality (Advanced Edition)

**Note:** DLT requires a **Databricks Premium** workspace.

**DLT Dataset Types**

DLT supports three dataset types.

**1. Streaming Table**

Used for:

- Streaming workloads

- Incremental processing

- Continuously arriving data

Characteristics:

- Reads using spark.readStream

- Supports append operations

- Permanently stored

Example:

@dlt.table\
def orders_bronze():\
return spark.readStream.table("dev.etl.orders_raw")

**2. Materialized View**

Used for:

- Batch transformations

- Aggregations

- Joins

- Cleansing

Characteristics:

- Reads using spark.read

- Stores computed results

- Recomputed whenever pipeline runs

Example:

@dlt.table\
def customer_bronze():\
return spark.read.table("dev.etl.customer_raw")

**3. View**

Used for:

- Temporary transformations

- Intermediate joins

- Logic reused later

Characteristics:

- Not stored in Unity Catalog

- Exists only during pipeline execution

Example:

@dlt.view\
def joined_view():

**Bronze → Silver → Gold Architecture**

The demonstration builds a classic Medallion Architecture.

Orders Raw\
\\\
\\\
---\> Bronze\
/\
Customers Raw\
/\
\
Bronze\
\|\
\| Join\
\|\
View\
\
Silver\
\|\
Aggregation\
\|\
Gold

Pipeline flow:

Orders Raw\
\|\
Streaming Table\
\|\
Orders Bronze\
\|\
\
Customers Raw\
\|\
Materialized View\
\|\
Customer Bronze\
\|\
\
Join View\
\|\
Joined Silver\
\|\
Aggregate\
\|\
Orders Aggregated Gold

**Reading Streaming vs Batch**

Streaming source:

spark.readStream.table(...)

Produces:

- Streaming Table

Batch source:

spark.read.table(...)

Produces:

- Materialized View

This is the primary distinction demonstrated in the lesson.

**DLT Decorators**

**Streaming Table**

@dlt.table

Creates:

- Streaming table

- Materialized view

**View**

@dlt.view

Creates:

- Temporary pipeline view

**Table Properties**

Tables can include metadata.

Example:

@dlt.table(\
table_properties={\
"quality":"bronze"\
},\
comment="Orders Bronze Table"\
)

Useful for:

- Bronze/Silver/Gold labels

- Documentation

- Governance

**Reading Tables Created in Same Pipeline**

DLT uses the keyword:

LIVE

Example:

spark.read.table("LIVE.customer_bronze")

or

spark.read.table("LIVE.orders_bronze")

This references datasets created earlier within the same DLT pipeline.

**Building the Pipeline**

The lesson demonstrates:

**Step 1**

Read Orders

↓

Streaming Bronze

**Step 2**

Read Customers

↓

Materialized Bronze

**Step 3**

Join them

↓

Temporary View

**Step 4**

Add Insert Timestamp

↓

Silver

**Step 5**

Aggregate

↓

Gold

The final Gold table groups by **Market Segment** and counts orders.

**Creating a DLT Pipeline**

Instead of running notebooks directly, DLT executes through a **DLT Pipeline**.

Create one by:

New\
↓\
Delta Live Tables Pipeline

Configure:

- Pipeline name

- Notebook

- Unity Catalog

- Schema

- Compute

- Pipeline mode

**Product Editions**

Three editions exist.

**Core**

Supports:

- Streaming Tables

- Materialized Views

- Aggregations

Does **not** support:

- CDC

- Data Quality

**Pro**

Adds:

- Change Data Capture (CDC)

Still lacks:

- Data Quality expectations

**Advanced**

Supports everything:

- CDC

- Data Quality

- Expectations

- Full DLT capabilities

**Pipeline Modes**

**Triggered**

Runs:

- Once

- On schedule

Best for:

- Batch ETL

**Continuous**

Runs continuously.

Best for:

- Streaming pipelines

**Unity Catalog Integration**

DLT writes datasets directly into Unity Catalog.

Example:

Catalog\
\
↓\
\
Schema\
\
↓\
\
Bronze Tables\
\
↓\
\
Silver Tables\
\
↓\
\
Gold Tables

If the schema does not exist, DLT can create it automatically.

**Development vs Production Mode**

**Development Mode**

- Cluster stays alive

- Easier debugging

- Faster reruns

Useful while developing pipelines.

**Production Mode**

After pipeline finishes:

- Cluster terminates automatically

Designed to minimize costs in production.

**Debugging Example**

The lesson demonstrates fixing two errors.

**Error 1**

count not defined

Solution:

from pyspark.sql.functions import count

**Error 2**

Wrong column:

c_orderkey

Correct column:

o_orderkey

Because the cluster remained active in Development Mode, fixes could be tested immediately without restarting resources.

**Pipeline Visualization (DAG)**

DLT automatically generates a Directed Acyclic Graph (DAG).

Example flow:

Customer Bronze\
\\\
\\\
Join View\
/\
Orders Bronze\
\|\
Joined Silver\
\|\
Aggregated Gold

The DAG shows:

- Dataset dependencies

- Processing order

- Record counts

- Execution progress

**Final Output**

After execution:

Created datasets:

- Orders Bronze (Streaming Table)

- Customer Bronze (Materialized View)

- Joined Silver (Materialized View)

- Orders Aggregated Gold (Materialized View)

Not created:

- Join View

The view is temporary and exists only during pipeline execution.

**Key Takeaways**

- **Delta Live Tables (DLT)** simplifies ETL by letting developers focus on transformations while Databricks manages orchestration, clusters, retries, and pipeline execution.

- DLT supports three dataset types:

  - **Streaming Tables** for incremental/streaming data

  - **Materialized Views** for batch transformations

  - **Views** for temporary intermediate logic

- Pipelines commonly follow the **Bronze → Silver → Gold** Medallion architecture.

- Use **spark.readStream** for streaming inputs and **spark.read** for batch inputs.

- Reference datasets within the same pipeline using the **LIVE** keyword.

- DLT pipelines run through a dedicated **Delta Live Tables Pipeline**, not on an all-purpose cluster.

- **Core**, **Pro**, and **Advanced** editions provide progressively more features, including CDC and data quality.

- **Development Mode** keeps clusters running for rapid debugging, while **Production Mode** automatically shuts them down after execution.

- DLT automatically generates a dependency graph (DAG), manages execution order, and writes persistent Bronze, Silver, and Gold datasets into Unity Catalog, while temporary views remain internal to the pipeline.

# [README](./../../../README.md)
