# EXPLANATION 37 7

**Question 7**

**What happens after a masking function is attached to a column in a Unity Catalog table?**

**Correct Answer:** **C. Unity Catalog automatically applies the masking function whenever the column is queried.**

**Explanation**

Once a mask is attached to a column using SQL, Unity Catalog automatically evaluates the masking function for every query that references that column. Users do not need to call the function explicitly.

**Why the Correct Answer is Correct**

The enforcement is automatic, ensuring consistent protection across all queries.

**Why the Other Answers Are Wrong**

The incorrect options imply that users must manually invoke the masking function or use a special view.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Unity+Catalog+column+masks

------------------------------------------------------------------------

# [README](./../../../README.md)
