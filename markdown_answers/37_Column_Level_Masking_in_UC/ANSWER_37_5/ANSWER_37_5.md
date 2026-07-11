# ANSWER 37 5

**Question 5**

**Which SQL construct is used in the lesson to determine whether the original phone number or the masked value should be returned?**

**A. JOIN ❌ Incorrect**

JOIN combines tables.

It doesn't make decisions.

**B. MERGE ❌ Incorrect**

MERGE updates data.

Not used for masking logic.

**C. CASE ✅ Correct**

Example:

CASE

WHEN authorized

THEN phone

ELSE 'XXX-XXX-XXXX'

END

CASE works like an IF statement.

If authorized:

Return:

555-123-4567

Otherwise:

Return:

XXX-XXX-XXXX

**D. GROUP BY ❌ Incorrect**

Used for aggregation.

**E. HAVING ❌ Incorrect**

Filters aggregated results.

**Why C is correct**

CASE allows the masking function to return different values depending on authorization.

# [README](./../../../README.md)
