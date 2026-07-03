# ANSWER 14 3

**Question 3**

**What is the primary benefit of using CREATE TABLE IF NOT EXISTS?**

**A. It automatically creates a backup table.** ❌ Incorrect

- No backup is created.

**B. It avoids errors if the table already exists.** ✅ Correct

Without it:

CREATE TABLE sales (...);

If the table already exists:

Error

With it:

CREATE TABLE IF NOT EXISTS sales (...);

If the table exists:

No error\
Nothing happens

This is especially useful in automation scripts.

**C. It converts the table into a Delta table.** ❌ Incorrect

- Delta is specified separately with USING DELTA.

**D. It deletes duplicate records automatically.** ❌ Incorrect

- It only creates tables.

**E. It enables time travel by default.** ❌ Incorrect

- Time Travel is a Delta Lake feature.

**Key Concept**

IF NOT EXISTS

↓

Safe to run multiple times.

# [README](./../../../README.md)
