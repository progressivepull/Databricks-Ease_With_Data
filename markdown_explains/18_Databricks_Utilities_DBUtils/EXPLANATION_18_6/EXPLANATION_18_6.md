# EXPLANATION 18 6

**Question 5**

**Which DBUtils command displays the beginning of a file without opening the entire file?**

**Correct Answer: C. dbutils.fs.head()**

**Explanation**

Instead of downloading the whole file:

dbutils.fs.head(path)

shows the first part of it.

Example

dbutils.fs.head("/Volumes/demo/employees.csv")

Output

id,name\
\
1,John\
\
2,Susan

------------------------------------------------------------------------

**Why is this useful?**

Imagine a 10 GB CSV.

You only need to verify:

- headers

- delimiter

- encoding

No need to load everything.

------------------------------------------------------------------------

**Similar Linux command**

head employees.csv

------------------------------------------------------------------------

**YouTube**

- <https://www.youtube.com/watch?v=zMUiDYgqlq0>

------------------------------------------------------------------------

# [README](./../../../README.md)
