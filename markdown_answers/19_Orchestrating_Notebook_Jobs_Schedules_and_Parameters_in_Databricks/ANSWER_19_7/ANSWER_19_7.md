# ANSWER 19 7

**Question 7**

**Which DBUtils command is used by the parent notebook to execute the child notebook?**

**A. dbutils.notebook.start()** ❌ Incorrect

- Invalid command.

**B. dbutils.notebook.run()** ✅ Correct

Example:

dbutils.notebook.run(\
"/ETL/Child",\
300,\
{"department":"Sales"}\
)

This:

- Starts the child notebook.

- Waits until it finishes.

- Returns the exit value.

**C. dbutils.notebook.execute()** ❌ Incorrect

- Invalid command.

**D. dbutils.jobs.run()** ❌ Incorrect

- Jobs are managed differently.

**E. dbutils.widgets.run()** ❌ Incorrect

- Widgets don't execute notebooks.

------------------------------------------------------------------------

**Memory Trick**

Parent

↓

Run Child

↓

run()

------------------------------------------------------------------------

# [README](./../../../README.md)
