# EXPLANATION 36 5

**Question 5**

**Why is the SQL EXISTS operator used in the row filter function?**

**Correct Answer:** **C. It returns a Boolean value indicating whether an authorization match exists.**

**Explanation**

EXISTS checks whether at least one matching authorization record is found.

Example:

RETURN EXISTS (

SELECT 1

FROM user_permissions

WHERE username = CURRENT_USER()

AND market = sales.market

);

If a matching row exists, the function returns **TRUE**, allowing the row to be visible. Otherwise, it returns **FALSE** and the row is filtered out.

**Why the Correct Answer is Correct**

Row filter functions must return a Boolean value, making EXISTS a natural choice.

**Why the Other Answers Are Wrong**

The incorrect options misunderstand the purpose of EXISTS or suggest it returns rows instead of a Boolean result.

**YouTube Video**\
https://www.youtube.com/watch?v=6KJwHkR7Y0Q

**Direct YouTube Link**\
https://www.youtube.com/watch?v=6KJwHkR7Y0Q

**YouTube Search**\
https://www.youtube.com/results?search_query=SQL+EXISTS+operator+tutorial

------------------------------------------------------------------------

# [README](./../../../README.md)
