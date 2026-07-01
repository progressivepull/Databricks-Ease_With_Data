# 15 Dalta Tables Merge and Upsets

**Delta Tables Merge (UPSERT) Operations**

This lesson introduces the **MERGE** operation in Delta Lake, one of its most powerful features. MERGE combines **INSERT**, **UPDATE**, and optional **DELETE** operations into a single atomic transaction, making it ideal for implementing incremental data loads, Change Data Capture (CDC), and Slowly Changing Dimension Type 1 (SCD Type 1) processing.

**Key Topics Covered**

**1. What is MERGE?**

The **MERGE** command is also known as:

- **UPSERT** (Update + Insert)

- **SCD Type 1** operation in data warehousing

MERGE compares a **source table** with a **target table** and performs actions based on whether matching keys are found.

**2. Source and Target Tables**

The lesson uses two tables:

**Target Table**

EMP

Contains the organization's current employee records.

**Source Table**

EMP_UPDATES

Contains:

- Updated employee records

- New employee records

The primary key used for matching is:

EMP_ID

**3. MERGE Logic**

MERGE evaluates three possible scenarios.

**Scenario 1: Matching Keys**

If the employee exists in both tables:

- Update the target record.

Example:

EMP\
1001\
\
EMP_UPDATES\
1001

Result:

- Salary and other fields are updated.

**Scenario 2: New Keys**

If the employee exists only in the source table:

- Insert the new record into the target table.

Example:

Source\
1006

Result:

- Employee 1006 is inserted.

**Scenario 3: Missing from Source**

If the employee exists only in the target table:

Possible actions include:

- Delete the record

- Mark the record inactive (soft delete)

- Ignore it

Delta Lake supports all three approaches.

**4. Writing a MERGE Statement**

The lesson constructs a MERGE using:

- Target table

- Source table

- Matching condition

- Update logic

- Insert logic

The merge compares records using:

EMP_ID

as the business key.

**5. Updating Existing Records**

When keys match:

WHEN MATCHED

the lesson updates:

- Employee salary

This demonstrates how MERGE performs updates without requiring separate UPDATE statements.

**6. Inserting New Records**

When keys do not match:

WHEN NOT MATCHED

the lesson inserts the entire source row.

Since both tables share the same schema, the shortcut:

INSERT \*

is used.

If schemas differ, explicit column mappings must be specified.

**7. MERGE Statistics**

After execution, Delta Lake reports statistics such as:

- Total affected rows

- Updated rows

- Inserted rows

In the demonstration:

- 3 rows updated

- 1 row inserted

This provides immediate feedback on the operation.

**8. Deleting Missing Records**

MERGE supports a third condition:

WHEN NOT MATCHED BY SOURCE

This identifies rows that exist in the target but not in the source.

The lesson demonstrates:

DELETE

Result:

Employees missing from the update table are removed from the target table.

**9. Hard Delete**

Using:

DELETE

permanently removes records from the target table.

Example:

Employees:

- 1003

- 1005

are deleted because they no longer appear in the source table.

**10. Soft Delete**

Instead of physically deleting rows, many data warehouses use **soft deletes**.

The lesson demonstrates this approach.

First:

A new column is added:

IS_ACTIVE

using:

ALTER TABLE\
ADD COLUMN

**11. Delta Schema Evolution**

When the new column is added:

- Existing rows automatically receive the new column.

- Existing data is not rewritten.

This demonstrates Delta Lake's **schema evolution** capability.

**12. MERGE for Soft Delete**

The MERGE statement is modified.

Instead of:

DELETE

it performs:

UPDATE\
SET IS_ACTIVE = 'N'

For rows present in both tables:

IS_ACTIVE = 'Y'

For rows missing from the source:

IS_ACTIVE = 'N'

This preserves historical records while identifying inactive employees.

**13. Explicit Inserts After Schema Changes**

After adding the new column:

The schemas no longer match.

Therefore:

INSERT \*

cannot be used.

Instead:

- Column names

- Column values

must be specified explicitly.

This ensures the new IS_ACTIVE column receives the correct default value.

**14. Additional MERGE Conditions**

MERGE conditions can include additional filters.

Example:

WHEN MATCHED\
AND IS_ACTIVE = 'Y'

This allows updates to occur only for active records.

Such conditional logic enables sophisticated business rules during incremental processing.

**MERGE Workflow**

<span class="mark">Source Table\
│\
▼\
Compare Business Key\
│\
├──────── Match\
│ │\
│ ▼\
│ UPDATE\
│\
├──────── No Match\
│ │\
│ ▼\
│ INSERT\
│\
└──────── Missing From Source\
│\
┌─────────┴─────────┐\
▼ ▼\
DELETE Soft Delete\
(IS_ACTIVE='N')</span>

**MERGE Conditions**

| **Condition**              | **Action**                                   |
|----------------------------|----------------------------------------------|
| WHEN MATCHED               | Update existing records                      |
| WHEN NOT MATCHED           | Insert new records                           |
| WHEN NOT MATCHED BY SOURCE | Delete or soft delete missing target records |

**Hard Delete vs. Soft Delete**

| **Hard Delete**          | **Soft Delete**     |
|--------------------------|---------------------|
| Removes row permanently  | Keeps row           |
| Data no longer available | History preserved   |
| Uses DELETE              | Uses UPDATE         |
| Smaller tables           | Better auditability |

**Key Takeaways**

- **MERGE** is Delta Lake's implementation of an **UPSERT**, combining inserts and updates into a single atomic operation.

- It is commonly used to implement **Slowly Changing Dimension (SCD) Type 1** processing in data warehousing.

- MERGE compares a **source table** and a **target table** using one or more matching keys.

- WHEN MATCHED updates existing records, while WHEN NOT MATCHED inserts new records into the target table.

- WHEN NOT MATCHED BY SOURCE provides a third option for handling target records that no longer appear in the source, allowing either **hard deletes** or **soft deletes**.

- **Schema evolution** enables Delta Lake to add new columns, such as IS_ACTIVE, without rewriting existing data.

- After schema changes, explicit column mappings are required during inserts because INSERT \* is no longer sufficient.

- MERGE supports additional conditional logic, making it flexible for implementing complex business rules during incremental data loading and synchronization.

# [README](./../../../README.md)
