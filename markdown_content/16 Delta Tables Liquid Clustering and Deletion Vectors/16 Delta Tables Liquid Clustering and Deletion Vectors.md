# 16 Delta Tables Liquid Clustering and Deletion Vectors

**Delta Tables – Deletion Vectors and Liquid Clustering**

This lesson introduces two advanced Delta Lake optimization features: **Deletion Vectors** and **Liquid Clustering**. These features improve performance by reducing unnecessary file rewrites and optimizing how large datasets are organized for querying.

**Key Topics Covered**

**1. Deletion Vectors**

A **Deletion Vector** is an optimization feature in Delta Lake that avoids rewriting entire Parquet files when rows are deleted.

**Traditional Delete Behavior**

Without deletion vectors:

- A DELETE operation rewrites every affected Parquet file.

- Even deleting a single row requires rewriting the entire file.

- This becomes inefficient for very large datasets.

Example:

Parquet File\
┌──────────────────────────┐\
│ 1,000,000 rows │\
│ Delete 1 row │\
└──────────────┬───────────┘\
▼\
Entire file rewritten

**How Deletion Vectors Work**

With deletion vectors enabled:

- Rows are **marked as deleted**.

- The Parquet file is **not rewritten immediately**.

- Future queries ignore the flagged rows.

- Physical removal happens later during maintenance operations such as **OPTIMIZE**.

Parquet File\
┌──────────────────────────┐\
│ Row 1 │\
│ Row 2 (Deleted Flag) │\
│ Row 3 │\
│ Row 4 │\
└──────────────────────────┘

This significantly reduces write operations.

**2. Creating a Sample Delta Table**

The lesson demonstrates reading a CSV file using the SQL utility:

READ_FILES()

The CSV data is then loaded into a Delta table using **CTAS (Create Table As Select)**.

**3. Viewing Table Properties**

Using:

DESCRIBE EXTENDED table_name;

the instructor verifies that the table property:

delta.enableDeletionVectors

is enabled.

**4. Disabling Deletion Vectors**

Deletion vectors are disabled using:

ALTER TABLE\
SET TBLPROPERTIES

Setting:

delta.enableDeletionVectors = false

returns the table to the traditional behavior where DELETE operations rewrite data files.

**5. Delete Without Deletion Vectors**

After deleting records:

DELETE FROM table\
WHERE ...

the Delta transaction history shows:

- Files removed

- Files added

- No deletion vectors

This confirms that Delta rewrote Parquet files.

**6. Delta History**

Using:

DESCRIBE HISTORY table_name;

the lesson examines Delta transaction metadata.

Operation metrics show:

- Files removed

- Files added

- Number of deletion vectors

These metrics help understand what occurred internally.

**7. Delete With Deletion Vectors**

After re-enabling deletion vectors and deleting additional records:

Delta History shows:

- No files rewritten

- Deletion vectors added

- Rows logically deleted

Instead of rewriting data files, Delta simply records which rows should be ignored.

**8. Physical Cleanup**

Eventually, maintenance operations such as:

OPTIMIZE table_name;

rewrite Parquet files and permanently remove rows marked by deletion vectors.

This combines efficient deletes with long-term storage optimization.

**Advantages of Deletion Vectors**

- Faster DELETE operations

- Fewer Parquet rewrites

- Reduced I/O

- Better performance on very large tables

- Automatic cleanup during maintenance

**Requirements**

Deletion Vectors require:

- **Delta Lake 2.3.0+**

- **Databricks Runtime 12.2 LTS or later**

**Liquid Clustering**

The second major topic is **Liquid Clustering**, a modern replacement for many partitioning and Z-Ordering scenarios.

**9. Why Liquid Clustering?**

Traditional optimization techniques include:

- Partitioning

- Z-Ordering

While effective, they often require:

- Manual optimization

- Rewriting data

- Ongoing maintenance

Liquid Clustering automatically reorganizes data as new records arrive.

**10. When to Use Liquid Clustering**

Liquid Clustering is recommended when:

- Data has **high-cardinality columns**

- Data grows rapidly

- Access patterns change over time

- Partitioning becomes inefficient

- Queries frequently filter or join on certain columns

Examples include:

- Invoice Number

- Customer ID

- Transaction ID

**11. Enabling Liquid Clustering**

For an existing table:

ALTER TABLE\
CLUSTER BY (invoice_number);

This designates **invoice_number** as the clustering column.

**12. Cluster History**

Running:

DESCRIBE HISTORY table_name;

shows:

- Cluster By operation

- Selected clustering column

- Protocol updates

This confirms that clustering has been enabled.

**13. Removing Clustering**

To disable Liquid Clustering:

ALTER TABLE\
CLUSTER BY NONE;

The table returns to standard behavior.

**14. Creating a Clustered Table**

A new table can also be clustered during creation:

CREATE TABLE ...\
CLUSTER BY (invoice_number);

The clustering column becomes part of the table definition.

**15. Viewing Cluster Metadata**

Using:

DESCRIBE EXTENDED table_name;

shows:

- Clustering Columns

The instructor notes:

- Multiple clustering columns are supported.

- Clustering columns must appear within the first **32 columns** of the table.

**16. Query Performance**

Queries filtering on the clustering column execute more efficiently.

Example:

SELECT \*\
FROM sales\
WHERE invoice_number = ...

As data grows to millions or billions of rows, Liquid Clustering significantly reduces query time.

**17. Automatic Maintenance**

One of Liquid Clustering's biggest advantages is that newly inserted data is automatically organized according to the clustering columns.

Unlike traditional optimization methods:

- No manual repartitioning

- No repeated ZORDER operations

- Less maintenance overhead

**Deletion Vectors vs Traditional Deletes**

| **Without Deletion Vectors** | **With Deletion Vectors** |
|------------------------------|---------------------------|
| Rewrites Parquet files       | Marks rows as deleted     |
| High I/O                     | Minimal I/O               |
| Slower DELETE operations     | Faster DELETE operations  |
| Immediate rewrite            | Cleanup during OPTIMIZE   |

**Liquid Clustering vs Traditional Optimization**

| **Traditional Partitioning / Z-Ordering** | **Liquid Clustering**    |
|-------------------------------------------|--------------------------|
| Manual optimization                       | Automatic optimization   |
| Frequent data rewrites                    | Incremental organization |
| Fixed partition strategy                  | Flexible clustering      |
| Higher maintenance                        | Lower maintenance        |

**Key Takeaways**

- **Deletion Vectors** improve DELETE performance by marking rows as deleted instead of immediately rewriting Parquet files.

- Physical removal of deleted rows occurs later during maintenance operations such as **OPTIMIZE**.

- Delta transaction history clearly shows whether deletes resulted in file rewrites or deletion vectors.

- Deletion Vectors require **Delta Lake 2.3+** or **Databricks Runtime 12.2 LTS+**.

- **Liquid Clustering** is a modern data organization technique that automatically optimizes storage based on selected clustering columns.

- It is particularly beneficial for large datasets with **high-cardinality columns**, changing access patterns, or rapidly growing data.

- Clustering can be enabled on existing tables using ALTER TABLE ... CLUSTER BY or during table creation with CREATE TABLE ... CLUSTER BY.

- Liquid Clustering reduces manual optimization efforts and helps maintain high query performance as data volumes grow.

# [README](./../../../README.md)
