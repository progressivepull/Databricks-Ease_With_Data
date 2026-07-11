# ANSWER 25 9

**Question 9**

**Which schema evolution mode stores unexpected columns inside a special rescued data column while allowing the stream to continue running?**

**A. Add New Columns ❌ Incorrect**

Automatically adds new columns to the schema.

Nothing is rescued.

------------------------------------------------------------------------

**B. None ❌ Incorrect**

Disables automatic schema evolution.

Unexpected columns aren't stored in \_rescued_data.

------------------------------------------------------------------------

**C. Rescue ✅ Correct**

Suppose Auto Loader expects:

Name

Age

Incoming file:

Name

Age

Salary

Department

Result:

| **Name** | **Age** | **\_rescued_data**                 |
|----------|---------|------------------------------------|
| John     | 30      | {"Salary":80000,"Department":"IT"} |

The stream keeps running.

No data is lost.

------------------------------------------------------------------------

**D. Fail on New Columns ❌ Incorrect**

Immediately stops the stream when unexpected columns appear.

Useful for strict schema enforcement.

------------------------------------------------------------------------

**E. Strict Mode ❌ Incorrect**

Not an Auto Loader schema evolution mode.

------------------------------------------------------------------------

**Why C is correct**

The **Rescue** mode preserves unexpected columns in \_rescued_data while allowing ingestion to continue.

------------------------------------------------------------------------

# [README](./../../../README.md)
