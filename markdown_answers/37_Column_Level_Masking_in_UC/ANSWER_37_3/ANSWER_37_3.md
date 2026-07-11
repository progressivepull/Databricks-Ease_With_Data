# ANSWER 37 3

**Question 3**

**Which built-in SQL function returns the identity of the user executing the current query?**

**A. CURRENT_ROLE() ❌ Incorrect**

Returns the active role where applicable.

Not the user.

**B. USER_NAME() ❌ Incorrect**

Not a Databricks SQL built-in function.

**C. CURRENT_USER() ✅ Correct**

Example:

SELECT CURRENT_USER();

Result:

john@company.com

Masking functions frequently use:

CURRENT_USER()

to determine whether a user should see masked or unmasked data.

**D. SESSION_EMAIL() ❌ Incorrect**

Not a valid function.

**E. ACTIVE_USER() ❌ Incorrect**

Also not a Databricks SQL function.

**Why C is correct**

CURRENT_USER() identifies the user running the query so security rules can be applied dynamically.

# [README](./../../../README.md)
