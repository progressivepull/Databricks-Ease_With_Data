# ANSWER 34 10

**Question 10**

**Which approach is recommended for repeatable, automated permission management in Unity Catalog?**

**A. Editing notebook source code ❌ Incorrect**

Permissions should not be embedded in notebooks.

**B. Using only the Catalog Explorer UI ❌ Incorrect**

The UI is convenient for occasional changes but is not ideal for automation or version control.

**C. Using SQL GRANT and REVOKE statements ✅ Correct**

Examples:

GRANT SELECT

ON TABLE sales.orders

TO analysts;

REVOKE MODIFY

ON TABLE sales.orders

FROM analysts;

Advantages:

- repeatable

- scriptable

- version-controlled

- automatable

- suitable for CI/CD pipelines

**D. Restarting the Metastore after each permission change ❌ Incorrect**

Permission changes take effect without restarting the metastore.

**E. Assigning permissions directly to individual users instead of groups ❌ Incorrect**

Best practice is to assign permissions to **groups**, not individual users.

Groups:

- simplify administration

- reduce maintenance

- scale better

- support least-privilege access

**Why C is correct**

Using SQL GRANT and REVOKE statements is the recommended approach for managing Unity Catalog permissions because it is **repeatable, auditable, and automatable**. Permission scripts can be stored in source control, reviewed, and executed consistently across development, test, and production environments, making them far more suitable for enterprise governance than manual changes through the UI.

# [README](./../../../README.md)
