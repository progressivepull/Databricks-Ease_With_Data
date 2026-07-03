# ANSWER 16 9

**Question 9**

**Which SQL command enables Liquid Clustering on an existing Delta table?**

**A. ENABLE CLUSTER invoice_number;** ❌ Incorrect

- Invalid SQL.

**B. CREATE CLUSTER invoice_number;** ❌ Incorrect

- No such command.

**C. ALTER TABLE table_name CLUSTER BY (invoice_number);** ✅ Correct

Example:

ALTER TABLE sales\
CLUSTER BY (invoice_number);

Now Delta Lake knows which column to organize around.

**D. OPTIMIZE TABLE CLUSTER invoice_number;** ❌ Incorrect

- Invalid syntax.

**E. CREATE INDEX invoice_number;** ❌ Incorrect

- Delta Lake does not use SQL indexes in this manner.

**Memory Trick**

Already Have Table?

↓

ALTER TABLE

↓

CLUSTER BY

# [README](./../../../README.md)
