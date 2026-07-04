# EXPLANATION 23 7

**Question 6**

**Where does COPY INTO maintain metadata about previously processed files?**

**Correct Answer: C. The Delta transaction log (\_delta_log)**

**Explanation**

Every Delta table contains a hidden folder named:

\_delta_log

The transaction log stores metadata such as:

- Files already loaded.

- Table version history.

- Schema changes.

- ACID transaction information.

When COPY INTO runs again, it checks \_delta_log to determine which files have already been ingested and skips them.

This is what enables idempotent behavior.

**YouTube**

- **Delta Lake Transaction Log Explained**\
  https://www.youtube.com/results?search_query=Delta+Lake+transaction+log

# [README](./../../../README.md)
