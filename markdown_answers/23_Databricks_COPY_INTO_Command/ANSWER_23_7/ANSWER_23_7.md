# ANSWER 23 7

**Question 7**

**How can COPY INTO perform simple transformations while loading data?**

**A. By using Delta Live Tables only** ❌ Incorrect

- DLT is a separate product.

**B. By wrapping the source data in a SELECT statement that performs transformations** ✅ Correct

Example:

COPY INTO employees\
\
FROM (\
\
SELECT\
\
UPPER(name),\
\
salary \* 1.05\
\
FROM ...\
\
)

Simple transformations include:

- Rename columns

- Change case

- Filter rows

- Compute values

All during ingestion.

**C. By enabling Photon** ❌ Incorrect

- Photon improves speed.

**D. By using VACUUM before loading** ❌ Incorrect

- VACUUM removes obsolete files.

**E. By creating a temporary view first** ❌ Incorrect

- A temporary view is optional, not required.

**Memory Trick**

Need Simple Transformation?

↓

SELECT

↓

COPY INTO

# [README](./../../../README.md)
