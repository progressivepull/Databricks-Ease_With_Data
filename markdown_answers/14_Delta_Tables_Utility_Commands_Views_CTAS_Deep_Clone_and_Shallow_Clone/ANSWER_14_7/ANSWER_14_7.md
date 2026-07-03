# ANSWER 14 7

**Question 7**

**Which statement best describes CTAS (Create Table As Select)?**

**A. It creates only a metadata reference to the original table.** ❌ Incorrect

- That's closer to how a view behaves.

**B. It creates a new table with copied data but may not preserve all Delta metadata.** ✅ Correct

Example:

CREATE TABLE sales_copy AS\
SELECT \*\
FROM sales;

CTAS copies:

- Rows

- Data

It may not preserve:

- Table properties

- Comments

- Constraints

- History

- Other metadata

**C. It creates only a SQL view.** ❌ Incorrect

- CTAS creates a real table.

**D. It copies only transaction history.** ❌ Incorrect

- History is not copied.

**E. It shares the same physical data files with the source table.** ❌ Incorrect

- CTAS creates new data files.

**Key Concept**

CTAS =

Copy Data\
\
Not Everything Else

# [README](./../../../README.md)
