# EXPLANATION 36 6

**Question 6**

**What type of value must a Unity Catalog row filter function return?**

**Correct Answer:** **D. Boolean (TRUE or FALSE)**

**Explanation**

Every row filter function evaluates each row individually and returns:

- **TRUE** → Row is visible.

- **FALSE** → Row is hidden.

This Boolean result determines whether each row is included in the query output.

**Why the Correct Answer is Correct**

Boolean values are required because row filters function as predicates.

**Why the Other Answers Are Wrong**

Returning strings, numbers, or tables would not tell Unity Catalog whether to keep or exclude a row.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Unity+Catalog+row+filter+boolean

------------------------------------------------------------------------

# [README](./../../../README.md)
