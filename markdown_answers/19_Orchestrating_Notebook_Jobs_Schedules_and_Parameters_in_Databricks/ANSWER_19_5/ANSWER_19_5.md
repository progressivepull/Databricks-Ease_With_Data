# ANSWER 19 5

**Question 5**

**How does the child notebook generate the name of the Delta table it writes?**

**A. It always writes to the same table.** ❌ Incorrect

- That would eliminate flexibility.

**B. It uses the employee ID as the table name.** ❌ Incorrect

- Employee IDs identify records, not tables.

**C. It dynamically builds the table name using the department parameter (for example, dev.branch.dept_sales).** ✅ Correct

Example:

Widget:

Sales

Generated table:

dev.branch.dept_sales

Widget:

HR

Generated table:

dev.branch.dept_hr

This allows one notebook to support many departments.

**D. It creates a random table name.** ❌ Incorrect

- Random names would be difficult to manage.

**E. It stores all departments in a single Delta table.** ❌ Incorrect

- The lesson specifically creates department-specific tables.

------------------------------------------------------------------------

**Memory Trick**

Department

↓

Build Table Name

------------------------------------------------------------------------

# [README](./../../../README.md)
