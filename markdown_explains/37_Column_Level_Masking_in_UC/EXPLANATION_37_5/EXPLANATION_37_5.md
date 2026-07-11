# EXPLANATION 37 5

**Question 5**

**Which SQL construct is used in the lesson to determine whether the original phone number or the masked value should be returned?**

**Correct Answer:** **C. CASE**

**Explanation**

A masking function commonly uses a CASE expression:

CASE

WHEN authorized THEN phone_number

ELSE 'XXX-XXX-1234'

END

The CASE expression returns either:

- the original value, or

- a masked value.

**Why the Correct Answer is Correct**

CASE performs conditional logic directly in SQL and is widely used in masking functions. Databricks recommends keeping masking UDFs simple, with CASE expressions preferred where practical.

**Why the Other Answers Are Wrong**

The other constructs do not provide straightforward conditional branching for this scenario.

**YouTube Video**\
https://www.youtube.com/watch?v=9K4Qx8mX4iQ

**Direct YouTube Link**\
https://www.youtube.com/watch?v=9K4Qx8mX4iQ

**YouTube Search**\
https://www.youtube.com/results?search_query=SQL+CASE+statement+tutorial

------------------------------------------------------------------------

# [README](./../../../README.md)
