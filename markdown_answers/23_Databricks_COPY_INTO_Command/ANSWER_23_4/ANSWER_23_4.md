# ANSWER 23 4

**Question 4**

**Why does the lesson create a placeholder Delta table before using COPY INTO?**

**A. To permanently disable schema inference** ❌ Incorrect

- Schema inference is actually the goal.

**B. To create an empty table without a predefined schema so COPY INTO can infer it automatically** ✅ Correct

Example:

CREATE TABLE sales;

Initially:

Empty

When COPY INTO loads the first file:

Reads CSV\
\
↓\
\
Determines Columns\
\
↓\
\
Creates Schema

This simplifies loading new datasets.

**C. To optimize query performance** ❌ Incorrect

- Placeholder tables do not improve performance.

**D. To convert CSV files into Parquet before loading** ❌ Incorrect

- COPY INTO loads directly.

**E. To create a backup of the source files** ❌ Incorrect

- No backup is created.

**Memory Trick**

Empty Table

↓

COPY INTO

↓

Infer Schema

# [README](./../../../README.md)
