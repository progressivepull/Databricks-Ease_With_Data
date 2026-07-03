# ANSWER 19 6

**Question 6**

**Which DBUtils command allows the child notebook to return a value to the parent notebook?**

**A. dbutils.widgets.exit()** ❌ Incorrect

- Widgets don't return notebook status.

**B. dbutils.fs.return()** ❌ Incorrect

- File System commands don't return notebook results.

**C. dbutils.notebook.exit()** ✅ Correct

Example:

dbutils.notebook.exit("SUCCESS")

Parent notebook:

status =\
dbutils.notebook.run(...)

Result:

SUCCESS

**D. dbutils.notebook.complete()** ❌ Incorrect

- Invalid command.

**E. dbutils.widgets.get()** ❌ Incorrect

- Retrieves widget values.

------------------------------------------------------------------------

**Memory Trick**

Child finishes

↓

exit()

------------------------------------------------------------------------

# [README](./../../../README.md)
