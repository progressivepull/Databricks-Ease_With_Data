# ANSWER 23 3

**Question 3**

**What does it mean that COPY INTO is idempotent?**

**A. It rewrites all files every time it runs.** ❌ Incorrect

- That would waste time and create duplicates.

**B. It creates duplicate records to ensure consistency.** ❌ Incorrect

- Idempotency is the opposite of creating duplicates.

**C. Running the command multiple times does not reload previously processed files.** ✅ Correct

Example:

Folder:

file1.csv\
\
file2.csv

First run:

Loads\
\
file1\
\
file2

Later:

file3.csv

Second run:

Loads\
\
file3\
\
Skips\
\
file1\
\
file2

This prevents duplicate loading.

**D. It requires manual cleanup after every execution.** ❌ Incorrect

- No manual cleanup is required for already processed files.

**E. It automatically deletes the source files after loading.** ❌ Incorrect

- Source files remain unless you delete them.

**Memory Trick**

Idempotent

↓

Safe to Run Again

# [README](./../../../README.md)
