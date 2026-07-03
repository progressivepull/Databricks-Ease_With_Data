# ANSWER 18 4

**Question 4**

**Which DBUtils command lists the contents of a directory?**

**A. dbutils.fs.head()** ❌ Incorrect

- Reads the beginning of a file.

**B. dbutils.fs.cp()** ❌ Incorrect

- Copies files.

**C. dbutils.fs.mkdirs()** ❌ Incorrect

- Creates folders.

**D. dbutils.fs.ls()** ✅ Correct

Example:

dbutils.fs.ls("/Volumes/main/default/files")

Output:

images/\
\
sales.csv\
\
notes.txt\
\
report.pdf

Very similar to:

ls

in Linux.

**E. dbutils.fs.mv()** ❌ Incorrect

- Moves files.

**Memory Trick**

Linux

ls

Databricks

dbutils.fs.ls()

# [README](./../../../README.md)
