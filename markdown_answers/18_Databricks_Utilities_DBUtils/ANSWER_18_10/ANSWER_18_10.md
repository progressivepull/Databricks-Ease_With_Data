# ANSWER 18 10

**Question 10**

**Which DBUtils notebook command returns a status value or result back to the calling notebook?**

**A. dbutils.notebook.return()** ❌ Incorrect

- No such command.

**B. dbutils.notebook.finish()** ❌ Incorrect

- Invalid.

**C. dbutils.notebook.complete()** ❌ Incorrect

- Invalid.

**D. dbutils.notebook.exit()** ✅ Correct

Example:

Notebook B:

dbutils.notebook.exit("SUCCESS")

Notebook A:

status =\
dbutils.notebook.run(...)

Result:

status == "SUCCESS"

This is how child notebooks communicate results back to the parent notebook.

**E. dbutils.notebook.close()** ❌ Incorrect

- Invalid.

**Memory Trick**

Run

↓

Exit

Notebook A\
\
↓\
\
run()\
\
↓\
\
Notebook B\
\
↓\
\
exit("SUCCESS")\
\
↓\
\
Notebook A receives SUCCESS

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| Languages that support DBUtils | **Python, Scala, and R** |
| Show all DBUtils modules | dbutils.help() |
| File system module | dbutils.fs |
| List directory contents | dbutils.fs.ls() |
| Preview the beginning of a file | dbutils.fs.head() |
| Widgets | Accept runtime notebook parameters |
| Read a widget value | dbutils.widgets.get() |
| Secrets | Securely retrieve passwords, API keys, tokens, and other sensitive values |
| Run another notebook | dbutils.notebook.run() |
| Return a value to the calling notebook | dbutils.notebook.exit() |

# [README](./../../../README.md)
