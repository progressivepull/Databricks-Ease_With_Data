# ANSWER 18 6

**Question 6**

**What is the primary purpose of DBUtils Widgets?**

**A. To optimize Spark jobs automatically** ❌ Incorrect

- Widgets don't optimize anything.

**B. To manage cluster permissions** ❌ Incorrect

- Permissions are managed separately.

**C. To allow notebooks to accept runtime input parameters** ✅ Correct

Example:

dbutils.widgets.text(\
"name",\
"John"\
)

Later:

name = dbutils.widgets.get("name")

Now the notebook can run with different values.

Common uses:

- Date parameters

- Environment names

- File paths

- Customer IDs

This allows one notebook to be reused many times.

**D. To store Delta transaction logs** ❌ Incorrect

- Delta tables handle transaction logs.

**E. To create Unity Catalog objects** ❌ Incorrect

- Widgets only collect user input.

**Memory Trick**

Widgets

↓

Notebook Parameters

# [README](./../../../README.md)
