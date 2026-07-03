# ANSWER 19 2

**Question 2**

**Which DBUtils command is used to create a notebook parameter (widget)?**

**A. dbutils.widgets.get()** ❌ Incorrect

- get() retrieves an existing widget value.

- It does **not** create a widget.

**B. dbutils.notebook.run()** ❌ Incorrect

- Executes another notebook.

- Doesn't create widgets.

**C. dbutils.widgets.text()** ✅ Correct

Example:

dbutils.widgets.text(\
"department",\
"Sales"\
)

Creates a text box like:

Department\
\[ Sales \]

Users can change the value before running the notebook.

**D. dbutils.notebook.exit()** ❌ Incorrect

- Returns a value from the notebook.

**E. dbutils.fs.head()** ❌ Incorrect

- Reads the beginning of a file.

------------------------------------------------------------------------

**Memory Trick**

Create Widget

↓

text()

Read Widget

↓

get()

------------------------------------------------------------------------

# [README](./../../../README.md)
