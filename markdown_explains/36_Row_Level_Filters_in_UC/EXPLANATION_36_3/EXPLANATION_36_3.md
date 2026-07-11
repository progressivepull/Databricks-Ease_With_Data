# EXPLANATION 36 3

**Question 3**

**Which built-in Databricks SQL function returns the identity of the user executing the query?**

**Correct Answer:** **C. CURRENT_USER()**

**Explanation**

CURRENT_USER() returns the identity of the user executing the SQL statement. It is commonly used in row filter functions to implement dynamic security rules based on the current user.

Example:

SELECT CURRENT_USER();

**Why the Correct Answer is Correct**

The function identifies the current user so the row filter can determine which records should be visible.

**Why the Other Answers Are Wrong**

The other functions either do not exist or return unrelated information.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+CURRENT_USER+function

------------------------------------------------------------------------

# [README](./../../../README.md)
