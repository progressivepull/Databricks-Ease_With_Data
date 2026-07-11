# ANSWER 25 10

**Question 10**

**Which hidden metadata column can be used to record the source filename for each ingested row?**

**A. \_metadata.file_path ❌ Incorrect**

\_metadata.file_path stores the **full path** to the source file, for example:

abfss://sales/2026/orders.csv

It is **not** just the filename.

------------------------------------------------------------------------

**B. \_metadata.source ❌ Incorrect**

No such hidden metadata column exists.

------------------------------------------------------------------------

**C. \_metadata.file_name ✅ Correct**

This hidden metadata column stores only the source filename.

Example:

orders_2026_07.csv

customers.csv

sales.parquet

It is commonly used for:

- auditing

- troubleshooting

- data lineage

- tracking which file produced each record

Example:

from pyspark.sql.functions import col

df = (

spark.readStream

.format("cloudFiles")

.option("cloudFiles.format", "csv")

.load("/input")

.select(

"\*",

col("\_metadata.file_name").alias("source_file")

)

)

------------------------------------------------------------------------

**D. \_metadata.filename_id ❌ Incorrect**

No such metadata column exists.

------------------------------------------------------------------------

**E. \_metadata.input_file ❌ Incorrect**

This is not a valid hidden metadata column. Spark provides functions such as input_file_name() in some contexts, but Auto Loader's hidden metadata column for the filename is \_metadata.file_name.

------------------------------------------------------------------------

**Why C is correct**

\_metadata.file_name captures the original source filename for each ingested row, making it valuable for auditing, lineage, and debugging data ingestion pipelines.

# [README](./../../../README.md)
