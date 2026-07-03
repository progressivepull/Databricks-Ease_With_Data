# ANSWER 23 8

**Question 8**

**What happens when a new source file is added to the landing folder and COPY INTO is executed again?**

**A. All files are reprocessed.** ❌ Incorrect

- That would create duplicate data.

**B. Only the new file is processed while previously loaded files are skipped.** ✅ Correct

Example:

Yesterday:

sales1.csv\
\
sales2.csv

Today:

sales3.csv

Second execution:

Loads\
\
sales3.csv\
\
Skips\
\
sales1.csv\
\
sales2.csv

This is the benefit of idempotency.

**C. The Delta table is recreated from scratch.** ❌ Incorrect

- The table continues to grow.

**D. Existing records are deleted before loading.** ❌ Incorrect

- Existing records remain.

**E. COPY INTO fails because duplicate files exist.** ❌ Incorrect

- Duplicate processing is automatically avoided.

**Memory Trick**

New File

↓

Load

Old Files

↓

Skip

# [README](./../../../README.md)
