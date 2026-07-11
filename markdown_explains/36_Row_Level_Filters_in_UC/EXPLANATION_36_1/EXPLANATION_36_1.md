# EXPLANATION 36 1

**Question 1**

**What is the primary purpose of Row-Level Security (RLS) in Unity Catalog?**

**Correct Answer:** **C. To restrict which rows each user can view within the same table**

**Explanation**

Row-Level Security (RLS) allows multiple users to query the **same physical table**, but each user sees only the rows they are authorized to access. Unity Catalog implements RLS using **row filter functions**, which evaluate a Boolean expression for each row at query time.

**Why the Correct Answer is Correct**

RLS:

- Restricts rows instead of entire tables.

- Lets all users query one shared table.

- Enforces security automatically during query execution.

- Eliminates the need to duplicate data for different user groups.

**Why the Other Answers Are Wrong**

- They describe table-level or column-level security rather than row-level filtering.

- They imply separate copies of data are required.

- They confuse authentication with data filtering.

**YouTube Video**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**Direct YouTube Link**\
https://www.youtube.com/watch?v=Ik4m9zV1xJY

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+Row+Level+Security+Unity+Catalog

------------------------------------------------------------------------

# [README](./../../../README.md)
