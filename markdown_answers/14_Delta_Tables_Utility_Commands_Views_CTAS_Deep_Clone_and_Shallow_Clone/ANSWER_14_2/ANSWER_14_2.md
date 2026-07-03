# ANSWER 14 2

**Question 2**

**Which PySpark command checks whether a table exists?**

**A. spark.table.exists()** ❌ Incorrect

- No such PySpark API exists.

**B. spark.catalog.tableExists()** ✅ Correct

Example:

spark.catalog.tableExists("sales.orders")

Returns:

True

or

False

This is the standard PySpark method.

**C. spark.sql.tableExists()** ❌ Incorrect

- spark.sql() executes SQL strings.

- It has no tableExists() method.

**D. dbutils.fs.tableExists()** ❌ Incorrect

- dbutils.fs works with files and directories.

- It knows nothing about SQL tables.

**E. spark.read.tableExists()** ❌ Incorrect

- spark.read loads data.

- It does not check metadata.

**Memory Trick**

Tables belong to the Spark **Catalog**.

spark.catalog.tableExists()

# [README](./../../../README.md)
