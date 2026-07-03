# ANSWER 18 9

**Question 9**

**Which DBUtils notebook command executes another notebook as part of a workflow?**

**A. dbutils.notebook.start()** ❌ Incorrect

- Invalid.

**B. dbutils.notebook.execute()** ❌ Incorrect

- Invalid.

**C. dbutils.notebook.run()** ✅ Correct

Example:

result =\
dbutils.notebook.run(\
"/ETL/LoadData",\
300,\
{"date":"2026-07-02"}\
)

This:

- Runs another notebook

- Waits for completion

- Receives its return value

This is widely used in workflows.

**D. dbutils.notebook.call()** ❌ Incorrect

- Invalid.

**E. dbutils.notebook.open()** ❌ Incorrect

- Invalid.

**Memory Trick**

Notebook

↓

Run

Another Notebook

# [README](./../../../README.md)
