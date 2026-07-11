# ANSWER 24 10

**Question 10**

**Which schema evolution mode stores unexpected columns in the \_rescued_data column without failing the stream?**

**A. addNewColumns** ❌ Incorrect

Automatically adds new columns to the schema.

No rescued data column.

------------------------------------------------------------------------

**B. none** ❌ Incorrect

No schema evolution.

Unexpected columns are ignored or handled differently.

------------------------------------------------------------------------

**C. mergeSchema** ❌ Incorrect

Used when writing Delta tables.

Not an Auto Loader schema evolution mode.

------------------------------------------------------------------------

**D. failOnNewColumns** ❌ Incorrect

Stops the stream when new columns appear.

Useful when strict schema enforcement is required.

------------------------------------------------------------------------

**E. rescue** ✅ Correct

Unexpected columns are stored in:

\_rescued_data

The stream continues without failure.

Example:

Incoming file:

Name

Age

Salary

Expected schema:

Name

Age

Result:

| **Name** | **Age** | **\_rescued_data** |
|----------|---------|--------------------|
| John     | 35      | {"Salary":80000}   |

No data is lost, and the pipeline continues running.

------------------------------------------------------------------------

**Why E is correct**

The rescue schema evolution mode preserves unexpected fields by placing them in the \_rescued_data column, allowing ingestion to continue without interrupting the stream.

# [README](./../../../README.md)
