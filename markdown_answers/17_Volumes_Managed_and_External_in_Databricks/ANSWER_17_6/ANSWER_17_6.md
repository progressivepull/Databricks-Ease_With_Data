# ANSWER 17 6

**Question 6**

**Which DBUtils command is used to copy files into a Unity Catalog volume?**

**A. dbutils.fs.cp()** ✅ Correct

Example:

dbutils.fs.cp(\
"/tmp/file.csv",\
"/Volumes/main/files/input/file.csv"\
)

Copies one file to another location.

**B. dbutils.fs.put()** ❌ Incorrect

- Creates small text files.

- Not typically used for copying existing files.

**C. dbutils.fs.mv()** ❌ Incorrect

- Moves files instead of copying them.

**D. dbutils.fs.head()** ❌ Incorrect

- Reads file contents.

**E. dbutils.fs.mount()** ❌ Incorrect

- Mounts storage.

- Unity Catalog Volumes eliminate much of the need for mounts.

------------------------------------------------------------------------

**Memory Trick**

Copy

↓

cp

------------------------------------------------------------------------

# [README](./../../../README.md)
