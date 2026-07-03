# ANSWER 22 7

**Question 7**

**What is the difference between Task Parameters and Job Parameters?**

**A. Task Parameters are shared across all jobs, while Job Parameters apply only to SQL tasks.** ❌ Incorrect

- This reverses the relationship.

**B. Job Parameters are automatically available to every task, while Task Parameters apply only to individual tasks.** ✅ Correct

Example:

Job Parameter:

Environment = Production

Every task can use it.

Task Parameter:

Department = Sales

Only one task receives it.

Think:

Job Parameter\
\
↓\
\
Everyone\
\
Task Parameter\
\
↓\
\
One Task

**C. Task Parameters can only be used with notebooks, while Job Parameters can only be used with Python scripts.** ❌ Incorrect

- Parameters work across task types.

**D. There is no difference between them.** ❌ Incorrect

- Their scope differs.

**E. Job Parameters are supported only for Delta Live Tables.** ❌ Incorrect

- Job Parameters apply broadly.

------------------------------------------------------------------------

**Memory Trick**

Job Parameter

↓

Global

Task Parameter

↓

Local

------------------------------------------------------------------------

# [README](./../../../README.md)
