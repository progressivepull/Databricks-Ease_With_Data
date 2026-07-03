# ANSWER 05 7

**Question 7**

**Why are Groups used in the Databricks Account Console?**

**A. To increase Spark performance** ❌ Incorrect

- Groups affect security, not compute performance.

**B. To automatically create workspaces** ❌ Incorrect

- Workspaces are created manually or through automation.

**C. To simplify permission management by assigning permissions to collections of users** ✅ **Correct**

- Rather than granting permissions individually, administrators assign permissions to groups.

- Benefits include:

  - Easier administration

  - Consistent security

  - Faster onboarding

  - Simpler auditing

**D. To replace Azure Active Directory** ❌ Incorrect

- Azure AD (Microsoft Entra ID) remains the identity provider.

- Databricks groups complement it.

**E. To manage Delta transaction logs** ❌ Incorrect

- Delta transaction logs track table changes.

- Groups have nothing to do with them.

**Key Concept**

Always assign permissions to **groups**, not individual users, whenever possible.

------------------------------------------------------------------------

# [README](./../../../README.md)
