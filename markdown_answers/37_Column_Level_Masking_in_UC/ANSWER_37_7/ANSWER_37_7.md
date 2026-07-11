# ANSWER 37 7

**Question 7**

**What happens after a masking function is attached to a column in a Unity Catalog table?**

**A. Users must manually call the masking function in every query. ❌ Incorrect**

Automatic masking is the primary benefit.

**B. The protected column is permanently replaced with masked values. ❌ Incorrect**

The underlying data never changes.

Only the displayed value changes.

**C. Unity Catalog automatically applies the masking function whenever the column is queried. ✅ Correct**

User writes:

SELECT phone

FROM customers;

Unity Catalog automatically evaluates:

Mask Function

↓

Authorized?

↓

Real Value

or

Masked Value

The user doesn't have to call the masking function directly.

**D. The table becomes read-only. ❌ Incorrect**

Masking doesn't affect write permissions.

**E. The column is removed from the table. ❌ Incorrect**

The column remains.

Only its displayed value changes.

**Why C is correct**

Masking is automatically enforced whenever the protected column is queried.

# [README](./../../../README.md)
