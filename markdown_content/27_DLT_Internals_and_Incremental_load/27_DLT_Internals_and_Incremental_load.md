# 27 DLT Internals and Incremental load

**Databricks Delta Live Tables (DLT) Internals & Incremental Load**

This lesson expands on the basics of **Delta Live Tables (DLT)** by demonstrating how DLT processes **incremental data**, automatically manages pipeline datasets, simplifies schema changes through its declarative framework, and integrates with **Unity Catalog** for lineage and metadata tracking. It also explains the internal architecture of streaming tables and materialized views.

------------------------------------------------------------------------

**1. DLT Automatically Manages Pipeline Datasets**

One of the biggest advantages of DLT is that it manages the lifecycle of all datasets created within a pipeline.

Every:

- Streaming Table

- Materialized View

- View

belongs to a specific **DLT Pipeline ID**.

Because of this:

- Creating a dataset in code automatically creates it in Unity Catalog.

- Removing a dataset from the pipeline code automatically removes it from the catalog.

- Developers never manually create or delete these tables.

DLT handles the entire lifecycle automatically.

------------------------------------------------------------------------

**2. Pipeline Runs Create Updates**

Every execution of a DLT pipeline creates an **Update**.

Each update records:

- Pipeline execution status

- Spark cluster information

- Spark UI

- Logs

- Metrics

- Event history

This provides complete monitoring and debugging for every pipeline run.

------------------------------------------------------------------------

**3. Processing Incremental Data**

To demonstrate incremental processing, the lesson inserts **10,000 new rows** into the orders_raw source table.

When the pipeline is executed again:

- Customer Bronze reads no new customer records.

- Orders Bronze reads only the newly inserted 10,000 rows.

- Silver and Gold layers are updated automatically.

The key point is that DLT processes **only new streaming data**, not the entire dataset.

------------------------------------------------------------------------

**4. Streaming Tables Process Only New Data**

Streaming tables remember previously processed records.

Example:

Orders Raw\
│\
New 10,000 Records\
│\
Streaming Table\
│\
Orders Bronze

Instead of reading millions of existing rows again, only the new records are processed.

Benefits:

- Faster execution

- Lower compute costs

- Efficient incremental ETL

------------------------------------------------------------------------

**5. Materialized Views Automatically Refresh**

Materialized views always produce the latest computed result.

Example:

Orders Bronze\
│\
Customer Bronze\
│\
Join\
│\
Silver\
│\
Aggregation\
│\
Gold

Whenever upstream data changes:

- Joins refresh automatically.

- Aggregations refresh automatically.

- Gold tables remain current.

No manual refresh logic is required.

------------------------------------------------------------------------

**6. Development Mode Makes Debugging Easy**

Because the pipeline runs in **Development Mode**, it can be attached directly to the notebook.

Developers can:

- Validate code

- Run the pipeline

- Debug errors

- Test changes

without recreating compute resources.

This greatly speeds up development.

------------------------------------------------------------------------

**7. Declarative Schema Evolution**

The lesson modifies the Gold aggregation by:

- Renaming an existing output column.

- Adding a new aggregation (SUM(order_total_price)).

In traditional ETL, this would often require:

- Altering target tables

- Updating schema definitions

- Modifying downstream logic

With DLT:

- Only the transformation code changes.

- DLT automatically updates the schema during pipeline execution.

This illustrates the power of the declarative programming model.

------------------------------------------------------------------------

**8. Automatic Validation**

Before running the pipeline, DLT performs validation.

In the lesson:

Error:

sum not defined

Solution:

from pyspark.sql.functions import sum

DLT detects code issues before full execution, reducing runtime failures.

------------------------------------------------------------------------

**9. Automatic Dataset Renaming**

The lesson renames:

joined_silver

to

order_silver

Only the notebook code changes.

DLT automatically:

- Removes the old dataset.

- Creates the new dataset.

- Updates pipeline metadata.

No manual cleanup is necessary.

------------------------------------------------------------------------

**10. Internal Storage Architecture**

Although users see Streaming Tables and Materialized Views, DLT stores data in hidden internal Delta tables.

Structure:

Unity Catalog\
│\
Materialized View\
│\
References\
│\
Databricks Internal Catalog\
│\
Internal Delta Table

Each visible dataset points to an internal Delta table managed by Databricks.

------------------------------------------------------------------------

**11. Databricks Internal Catalog**

Running a DLT pipeline creates an internal catalog.

It contains:

- Hidden Delta tables

- Pipeline metadata

- Internal storage objects

Developers normally do not interact with these tables directly, but they are the actual physical storage behind DLT datasets.

------------------------------------------------------------------------

**12. Streaming Tables Use Checkpoints**

Streaming tables maintain incremental processing through **checkpointing**.

Internal structure:

Streaming Table\
│\
Delta Table\
│\
DLT Metadata\
│\
Checkpoint

The checkpoint stores information about:

- Processed records

- Processing progress

- Stream offsets

This allows future runs to read only new data instead of reprocessing everything.

------------------------------------------------------------------------

**13. Materialized Views Store Computed Results**

Materialized views are backed by Delta tables.

They automatically maintain:

- Latest joins

- Latest aggregations

- Current computed values

Users query the materialized view, while DLT manages the underlying Delta storage transparently.

------------------------------------------------------------------------

**14. Pipeline Dependency Graph**

The execution flow looks like:

Orders Raw\
│\
Orders Bronze (Streaming)\
│\
├────────────┐\
│ │\
Customers Raw │\
│ │\
Customer Bronze │\
│ │\
└────Join────┘\
│\
Order Silver\
│\
Orders Aggregated Gold

DLT determines the execution order automatically based on dependencies.

------------------------------------------------------------------------

**15. Unity Catalog Lineage**

Unity Catalog automatically builds lineage graphs.

It tracks:

- Source tables

- Destination tables

- Intermediate transformations

- Notebook usage

- Column-level lineage

Example:

Orders Raw\
│\
Orders Bronze\
│\
Order Silver\
│\
Orders Aggregated Gold

Users can trace any dataset back to its original source.

------------------------------------------------------------------------

**16. Column-Level Lineage**

Unity Catalog also tracks how individual columns are derived.

For example:

Order Key\
│\
COUNT()\
│\
Count Orders

This helps with:

- Auditing

- Governance

- Impact analysis

- Regulatory compliance

------------------------------------------------------------------------

**17. Lineage Works Beyond DLT**

Lineage is a **Unity Catalog feature**, not a DLT-only feature.

It works for:

- DLT pipelines

- Standard Delta tables

- SQL transformations

- Other Unity Catalog-managed assets

This provides consistent governance across the entire data platform.

------------------------------------------------------------------------

**Key Takeaways**

- DLT automatically manages the lifecycle of all pipeline datasets through a unique **Pipeline ID**.

- Every pipeline execution creates an **Update** containing logs, metrics, Spark UI details, and execution history.

- **Streaming Tables** process only new data by using **checkpoints**, enabling efficient incremental ETL.

- **Materialized Views** automatically recompute joins and aggregations whenever upstream data changes.

- The declarative model allows developers to add columns, rename datasets, and evolve schemas by modifying only the transformation code—DLT handles the underlying table updates.

- DLT stores data in hidden **Databricks Internal Catalog** Delta tables while exposing Streaming Tables and Materialized Views through Unity Catalog.

- **Unity Catalog Lineage** provides end-to-end table and column-level data lineage, making it easy to trace data origins, understand transformations, and support governance and auditing

# [README](./../../../README.md)
