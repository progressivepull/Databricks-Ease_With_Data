# ANSWER 08 5

**Question 5**

**Which of the following is the highest-level data securable object in Unity Catalog?**

**A. Table** ❌ Incorrect

- Tables are individual data objects.

**B. Schema** ❌ Incorrect

- Schemas contain tables.

**C. Catalog** ✅ Correct

Catalogs are the highest **data securable** objects.

Permissions can be assigned at the catalog level.

Example:

Finance Catalog\
Payroll Schema\
Employees Table

Granting access to the Finance catalog can provide access to everything inside it, depending on inherited permissions.

**D. Volume** ❌ Incorrect

- Volumes store files.

- They are lower-level objects.

**E. View** ❌ Incorrect

- Views are virtual tables.

- They inherit governance from higher levels.

**Memory trick**

Catalog\
↓\
Schema\
↓\
Table

------------------------------------------------------------------------

# [README](./../../../README.md)
