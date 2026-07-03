# ANSWER 13 9

**Question 9**

**When an external table is dropped in Unity Catalog, what happens to the physical data files?**

**A. They are immediately deleted.** ❌ Incorrect

- Unity Catalog never deletes external data files when dropping an external table.

**B. They are retained permanently in the external storage location.** ✅ Correct

Example:

ADLS\
\
sales.delta\
customers.delta

Drop table:

DROP TABLE sales;

Result:

Metadata:

❌ Removed

Files:

✅ Still exist

The table can later be recreated by referencing the same location.

**C. They are moved to Unity Catalog managed storage.** ❌ Incorrect

- Unity Catalog never relocates external data automatically.

**D. They are compressed into Delta logs.** ❌ Incorrect

- Delta logs track transactions.

- They do not archive dropped data.

**E. They are archived in the Control Plane.** ❌ Incorrect

- Customer data is never stored in the Control Plane.

**Memory Trick**

External Table

↓

Drop Table

↓

Only metadata disappears

↓

Files stay in ADLS

------------------------------------------------------------------------

# [README](./../../../README.md)
