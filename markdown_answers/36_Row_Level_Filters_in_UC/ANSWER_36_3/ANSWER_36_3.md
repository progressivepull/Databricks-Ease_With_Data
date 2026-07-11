# ANSWER 36 3

**Question 3**

**Which built-in Databricks SQL function returns the identity of the user executing the query?**

**A. CURRENT_ROLE() ❌ Incorrect**

- Returns the current role (where supported), not the user identity.

------------------------------------------------------------------------

**B. CURRENT_EMAIL() ❌ Incorrect**

- Not a Databricks SQL function.

------------------------------------------------------------------------

**C. CURRENT_USER() ✅ Correct**

Example:

SELECT CURRENT_USER();

Result:

john@company.com

Row filters commonly use:

CURRENT_USER()

to determine which rows should be visible.

------------------------------------------------------------------------

**D. SESSION_USER() ❌ Incorrect**

- Depending on SQL dialects, similar functions may exist elsewhere, but in Databricks the lesson uses CURRENT_USER().

------------------------------------------------------------------------

**E. ACTIVE_USER() ❌ Incorrect**

Not a built-in Databricks SQL function.

------------------------------------------------------------------------

**Why C is correct**

CURRENT_USER() identifies the person executing the query, enabling user-specific security rules.

------------------------------------------------------------------------

# [README](./../../../README.md)
