# ANSWER 34 8

**Question 8**

**Which statement about ALL PRIVILEGES is correct?**

**A. It includes the ability to change object ownership. ❌ Incorrect**

Ownership is a separate capability.

**B. It includes the MANAGE privilege automatically. ❌ Incorrect**

MANAGE is intentionally excluded.

**C. It grants nearly every operational permission but does not include managing permissions or ownership. ✅ Correct**

ALL PRIVILEGES includes most operational actions, such as reading, modifying, or creating objects where applicable.

However, it **does not** include:

- MANAGE

- Ownership

This separation helps prevent accidental delegation of administrative control.

**D. It is equivalent to Metastore Administrator privileges. ❌ Incorrect**

Metastore Administrators have far broader authority.

**E. It allows only read operations. ❌ Incorrect**

ALL PRIVILEGES includes much more than read access.

**Why C is correct**

ALL PRIVILEGES provides broad operational access while reserving security administration and ownership for higher-level permissions.

# [README](./../../../README.md)
