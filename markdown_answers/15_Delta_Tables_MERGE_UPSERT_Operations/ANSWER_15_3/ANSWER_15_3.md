# ANSWER 15 3

**Question 3**

**In the lesson's MERGE example, which column is used as the business key to compare the source and target tables?**

**A. EMP_NAME** ❌ Incorrect

- Employee names can change.

- They are poor business keys.

**B. DEPARTMENT** ❌ Incorrect

- Many employees share departments.

**C. SALARY** ❌ Incorrect

- Salaries change frequently.

- Not unique.

**D. EMP_ID** ✅ Correct

A business key uniquely identifies a record.

Example:

EMP_ID\
\
1001\
\
1002\
\
1003

MERGE compares:

ON target.EMP_ID = source.EMP_ID

Everything else can change.

**E. IS_ACTIVE** ❌ Incorrect

- This indicates record status.

- It is not an identifier.

**Memory Trick**

MERGE needs a key.

Usually:

- CustomerID

- EmployeeID

- ProductID

- OrderID

------------------------------------------------------------------------

# [README](./../../../README.md)
