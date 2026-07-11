# ANSWER 25 5

**Question 5**

**What is the purpose of the following option?**

.option("pathGlobFilter", "\*.csv")

**A. Compress CSV files before loading them ❌ Incorrect**

It performs no compression.

------------------------------------------------------------------------

**B. Convert all file types into CSV format ❌ Incorrect**

It never converts file formats.

------------------------------------------------------------------------

**C. Process only CSV files while ignoring other file types ✅ Correct**

Suppose your folder contains:

sales.csv

orders.csv

notes.txt

image.png

customers.json

Using:

.option("pathGlobFilter", "\*.csv")

Auto Loader reads only:

sales.csv

orders.csv

Everything else is ignored.

------------------------------------------------------------------------

**D. Load only files larger than 1 MB ❌ Incorrect**

No size filtering occurs.

------------------------------------------------------------------------

**E. Rename CSV files during ingestion ❌ Incorrect**

Files are never renamed.

------------------------------------------------------------------------

**Why C is correct**

pathGlobFilter filters files by filename pattern before ingestion.

------------------------------------------------------------------------

# [README](./../../../README.md)
