# ANSWER 37 6

**Question 6**

**What type of value does a column masking function return?**

**A. Boolean (TRUE or FALSE) ❌ Incorrect**

Boolean values are used for **Row-Level Filters**, not masking.

**B. A complete table ❌ Incorrect**

Masking functions operate on individual column values.

**C. The same data type as the protected column, such as a string for phone numbers ✅ Correct**

Suppose:

Phone

is:

STRING

The function returns:

Authorized:

555-123-4567

Unauthorized:

XXX-XXX-4567

Still a STRING.

Likewise:

Salary:

DECIMAL

must return another DECIMAL.

**D. JSON only ❌ Incorrect**

No such requirement exists.

**E. An integer only ❌ Incorrect**

Depends entirely on the protected column's type.

**Why C is correct**

Masking functions must return the **same data type** as the column they protect.

# [README](./../../../README.md)
