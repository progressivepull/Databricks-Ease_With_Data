# EXPLANATION 19 7

**Question 6**

**Which DBUtils command allows the child notebook to return a value to the parent notebook?**

**Correct Answer: C. dbutils.notebook.exit()**

**Explanation**

When the child notebook finishes, it can return a value.

Example:

dbutils.notebook.exit("Completed Successfully")

The parent notebook receives:

result = dbutils.notebook.run(...)\
\
print(result)

Output:

Completed Successfully

Returned values can include:

- Success messages

- Error messages

- Record counts

- Processing status

- File names

**YouTube**

- **Databricks Notebook Exit and Return Values**\
  https://www.youtube.com/results?search_query=dbutils.notebook.exit+Databricks

# [README](./../../../README.md)
