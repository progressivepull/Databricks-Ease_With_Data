# ANSWER 19 3

**Question 3**

**Which DBUtils command retrieves the value entered into a widget?**

**A. dbutils.widgets.read()** ❌ Incorrect

- No such command exists.

**B. dbutils.widgets.get()** ✅ Correct

Example:

department =\
dbutils.widgets.get("department")

If the widget contains:

HR

then

department == "HR"

**C. dbutils.widgets.value()** ❌ Incorrect

- Invalid command.

**D. dbutils.notebook.get()** ❌ Incorrect

- Invalid command.

**E. dbutils.fs.get()** ❌ Incorrect

- File System module has no get() method for widgets.

------------------------------------------------------------------------

**Memory Trick**

Need the widget value?

↓

get()

------------------------------------------------------------------------

# [README](./../../../README.md)
