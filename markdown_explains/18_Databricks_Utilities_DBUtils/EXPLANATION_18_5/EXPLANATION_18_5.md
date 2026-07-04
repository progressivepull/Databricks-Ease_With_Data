# EXPLANATION 18 5

**Question 4**

**Which DBUtils command lists the contents of a directory?**

**Correct Answer: D. dbutils.fs.ls()**

**Explanation**

The command:

dbutils.fs.ls(path)

lists every file and folder inside a directory.

Example

dbutils.fs.ls("/Volumes/demo/files/")

Returns something similar to:

employees.csv\
\
sales.csv\
\
customers.csv

Many users display it nicely:

display(\
dbutils.fs.ls("/Volumes/demo/files/")\
)

------------------------------------------------------------------------

**Similar Linux command**

ls

------------------------------------------------------------------------

**YouTube**

- <https://www.youtube.com/watch?v=zMUiDYgqlq0>

------------------------------------------------------------------------

# [README](./../../../README.md)
