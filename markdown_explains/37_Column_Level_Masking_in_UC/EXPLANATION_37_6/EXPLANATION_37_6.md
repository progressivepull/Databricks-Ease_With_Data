# EXPLANATION 37 6

**Question 6**

**What type of value does a column masking function return?**

**Correct Answer:** **C. The same data type as the protected column, such as a string for phone numbers**

**Explanation**

A column masking function must return a value whose data type matches (or can be cast to) the protected column's data type. For example:

- Phone number column → returns a string.

- Salary column → returns a numeric value.

- Date column → returns a date.

**Why the Correct Answer is Correct**

Returning the correct data type ensures that queries continue to work correctly after masking.

**Why the Other Answers Are Wrong**

Returning a Boolean, table, or unrelated data type would make the column incompatible with its schema.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Unity+Catalog+column+mask+function

------------------------------------------------------------------------

# [README](./../../../README.md)
