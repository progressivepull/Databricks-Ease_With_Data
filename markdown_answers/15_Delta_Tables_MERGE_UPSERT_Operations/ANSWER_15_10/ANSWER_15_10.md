# ANSWER 15 10

**Question 10**

**What capability allows Delta Lake to add a new column such as IS_ACTIVE without rewriting existing data?**

**A. Delta Time Travel** ❌ Incorrect

- Time Travel queries previous versions.

- It doesn't add columns.

**B. Schema Evolution** ✅ Correct

Schema Evolution allows tables to evolve over time.

Example:

Old table:

EMP_ID\
NAME\
SALARY

New schema:

EMP_ID\
NAME\
SALARY\
IS_ACTIVE

Existing rows don't have to be rewritten immediately.

New rows receive values for the new column, while existing rows use the default or NULL until updated.

This makes schema changes much easier and more efficient than rewriting an entire dataset.

**C. Auto Loader** ❌ Incorrect

- Auto Loader ingests new files.

- It doesn't perform schema evolution on existing tables by itself.

**D. Liquid Clustering** ❌ Incorrect

- Liquid Clustering optimizes data layout.

- It has nothing to do with adding columns.

**E. Photon Acceleration** ❌ Incorrect

- Photon improves query performance.

- It does not modify schemas.

**Memory Trick**

Need to add a new column?

↓

Think:

Schema Evolution

------------------------------------------------------------------------

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| MERGE | Combines **INSERT**, **UPDATE**, and optional **DELETE** into a single atomic transaction |
| Other names for MERGE | **UPSERT** and **SCD Type 1** |
| Business key in the example | **EMP_ID** |
| Update existing rows | WHEN MATCHED |
| Insert new rows | WHEN NOT MATCHED |
| Handle target rows missing from the source | WHEN NOT MATCHED BY SOURCE |
| Hard delete | Permanently removes the record |
| Soft delete | Marks the record inactive (for example, IS_ACTIVE = FALSE) while preserving history |
| Why INSERT \* no longer works | The source and target schemas differ, so explicit column mappings are required |
| Add columns without rewriting existing data | **Schema Evolution** |

# [README](./../../../README.md)
