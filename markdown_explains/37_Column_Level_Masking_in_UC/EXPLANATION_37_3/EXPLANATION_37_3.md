# EXPLANATION 37 3

**Question 3**

**Which built-in SQL function returns the identity of the user executing the current query?**

**Correct Answer:** **C. CURRENT_USER()**

**Explanation**

CURRENT_USER() returns the identity of the currently authenticated user. Masking functions commonly use this function to determine whether the current user is authorized to see the original value or a masked value.

Example:

SELECT CURRENT_USER();

**Why the Correct Answer is Correct**

It enables dynamic security decisions based on the person executing the query.

**Why the Other Answers Are Wrong**

The other options either do not exist or return unrelated information.

**YouTube Video**\
https://www.youtube.com/watch?v=PyT6S_0RkY0

**Direct YouTube Link**\
https://www.youtube.com/watch?v=PyT6S_0RkY0

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+CURRENT_USER+function

------------------------------------------------------------------------

# [README](./../../../README.md)
