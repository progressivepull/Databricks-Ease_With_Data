# ANSWER 26 7

**Question 7**

**In the Medallion Architecture demonstrated in the lesson, what is the typical order of data refinement?**

**A. Gold → Silver → Bronze ❌ Incorrect**

This is backwards.

Gold is the final refined layer.

**B. Bronze → Gold → Silver ❌ Incorrect**

Gold comes after Silver.

**C. Silver → Bronze → Gold ❌ Incorrect**

Raw data always enters Bronze first.

**D. Bronze → Silver → Gold ✅ Correct**

Typical flow:

Raw Files

↓

Bronze

(raw ingestion)

↓

Silver

(cleaned & validated)

↓

Gold

(business-ready)

Each layer increases data quality.

**E. Raw → Gold → Bronze ❌ Incorrect**

Not how Medallion Architecture works.

**Why D is correct**

Bronze → Silver → Gold is the standard Databricks Medallion Architecture.

# [README](./../../../README.md)
