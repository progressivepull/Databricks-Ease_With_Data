# EXPLANATION 19 2

**Question 1**

**What is the primary purpose of the parent notebook in the lesson?**

**Correct Answer: C. To pass parameters, execute the child notebook, and receive returned results**

**Explanation**

The **parent notebook** acts like a project manager or orchestrator.

Its responsibilities are to:

- Pass parameters to the child notebook

- Execute the child notebook

- Wait for it to finish

- Receive a return value

- Decide what to do next

Example:

department = "Sales"\
\
result = dbutils.notebook.run(\
"/Shared/Employee_Load",\
timeout_seconds=300,\
arguments={"department": department}\
)\
\
print(result)

The parent notebook itself usually does very little data processing. Instead, it coordinates the workflow.

**Real-world example**

Imagine a company with five departments:

- Sales

- HR

- Finance

- Marketing

- IT

Instead of creating five different notebooks, the parent notebook loops through each department and calls the same child notebook with a different parameter.

Parent Notebook\
│\
├── Child Notebook (Sales)\
├── Child Notebook (HR)\
├── Child Notebook (Finance)\
├── Child Notebook (Marketing)\
└── Child Notebook (IT)

This design is easier to maintain and reuse.

**YouTube**

- **Databricks Notebook Workflows**\
  https://www.youtube.com/results?search_query=Databricks+Notebook+Workflows

- **Databricks Notebook Orchestration with dbutils.notebook.run**\
  https://www.youtube.com/results?search_query=dbutils.notebook.run+Databricks

# [README](./../../../README.md)
