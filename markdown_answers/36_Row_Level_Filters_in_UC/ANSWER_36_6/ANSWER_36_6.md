# ANSWER 36 6

**Question 6**

**What type of value must a Unity Catalog row filter function return?**

**A. Integer ❌ Incorrect**

Returning:

1

is not sufficient.

Unity Catalog expects TRUE or FALSE.

------------------------------------------------------------------------

**B. String ❌ Incorrect**

Returning:

"East"

doesn't indicate whether the row should be visible.

------------------------------------------------------------------------

**C. Table ❌ Incorrect**

Row filters operate on individual rows.

They don't return tables.

------------------------------------------------------------------------

**D. Boolean (TRUE or FALSE) ✅ Correct**

Every row asks:

Should I show this row?

Function returns:

TRUE

Visible.

or

FALSE

Hidden.

------------------------------------------------------------------------

**E. JSON object ❌ Incorrect**

JSON is not a valid return type for a row filter.

------------------------------------------------------------------------

**Why D is correct**

A row filter is essentially a Boolean test for each row.

------------------------------------------------------------------------

# [README](./../../../README.md)
