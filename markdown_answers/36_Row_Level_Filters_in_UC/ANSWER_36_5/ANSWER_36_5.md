# ANSWER 36 5

**Question 5**

**Why is the SQL EXISTS operator used in the row filter function?**

**A. It returns the first matching row from a table. ❌ Incorrect**

- EXISTS does **not** return rows.

- It returns a Boolean result.

------------------------------------------------------------------------

**B. It automatically updates the metadata table. ❌ Incorrect**

- EXISTS only checks for data.

- It never modifies tables.

------------------------------------------------------------------------

**C. It returns a Boolean value indicating whether an authorization match exists. ✅ Correct**

Example:

EXISTS (

SELECT 1

FROM security_rules

WHERE ...

)

Possible results:

TRUE

Authorized.

or

FALSE

Not authorized.

This Boolean value tells Unity Catalog whether to display each row.

------------------------------------------------------------------------

**D. It counts the number of authorized users. ❌ Incorrect**

- That's what:

COUNT()

would do.

------------------------------------------------------------------------

**E. It creates a temporary view for each user. ❌ Incorrect**

No views are created.

**Why C is correct**

EXISTS efficiently answers one question:

"Does an authorization rule exist?"

------------------------------------------------------------------------

# [README](./../../../README.md)
