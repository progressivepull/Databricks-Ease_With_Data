# ANSWER 37 1

**Question 1**

**What is the primary purpose of Column-Level Masking in Unity Catalog?**

**A. To remove sensitive columns from a table permanently ❌ Incorrect**

- Column masking **does not remove columns**.

- The column still exists in the table.

- Only the **value shown to the user** changes based on security rules.

Example:

| **Name** | **Phone**    |
|----------|--------------|
| John     | XXX-XXX-1234 |

The Phone column is still there—it is just masked.

**B. To restrict access to entire rows based on user identity ❌ Incorrect**

- This describes **Row-Level Security (RLS)**.

- RLS decides **which rows** users can see.

- Column masking decides **what values** users see in specific columns.

**C. To dynamically hide or mask sensitive column values while keeping the column visible ✅ Correct**

This is exactly what Column-Level Masking does.

Suppose the table contains:

| **Employee** | **Phone**    |
|--------------|--------------|
| John         | 555-123-4567 |

Manager sees:

| **Employee** | **Phone**    |
|--------------|--------------|
| John         | 555-123-4567 |

Regular employee sees:

| **Employee** | **Phone**    |
|--------------|--------------|
| John         | XXX-XXX-4567 |

Same table.

Same row.

Different value.

**D. To encrypt all data stored in Delta Lake ❌ Incorrect**

- Encryption protects stored data.

- Column masking changes **what users see**, not how data is stored.

**E. To create separate tables for different user groups ❌ Incorrect**

- One major benefit of masking is avoiding duplicate tables.

- Everyone queries the same table.

**Why C is correct**

Column-Level Masking protects **sensitive values** while allowing users to continue working with the same table structure.

# [README](./../../../README.md)
