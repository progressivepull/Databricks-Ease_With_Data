# ANSWER 14 5

**Question 5**

**What is the primary characteristic of a temporary view?**

**A. It stores a physical copy of the data.** ❌ Incorrect

- A view stores only SQL.

- It never copies data.

**B. It persists after the cluster is restarted.** ❌ Incorrect

- Temporary views disappear when the Spark session ends.

**C. It exists only during the current compute session.** ✅ Correct

Example:

df.createOrReplaceTempView("employees")

The view exists while the cluster/session is running.

When the session ends:

View disappears

**D. It automatically becomes a permanent view.** ❌ Incorrect

- Temporary and permanent views are different objects.

**E. It cannot execute SQL queries.** ❌ Incorrect

- That's exactly what views are for.

**Memory Trick**

Temporary View

↓

Current Session Only

# [README](./../../../README.md)
