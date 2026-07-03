# ANSWER 18 5

**Question 5**

**Which DBUtils command displays the beginning of a file without opening the entire file?**

**A. dbutils.fs.open()** ❌ Incorrect

- No such DBUtils command.

**B. dbutils.fs.read()** ❌ Incorrect

- Invalid command.

**C. dbutils.fs.head()** ✅ Correct

Example:

dbutils.fs.head(\
"/Volumes/main/default/files/customers.csv"\
)

Returns the first portion of the file.

Useful for:

- Checking CSV headers

- Previewing JSON

- Viewing logs

Without loading the full file.

**D. dbutils.fs.peek()** ❌ Incorrect

- Invalid command.

**E. dbutils.fs.preview()** ❌ Incorrect

- Invalid command.

**Memory Trick**

Head

↓

Top of File

# [README](./../../../README.md)
