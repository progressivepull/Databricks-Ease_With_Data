# ANSWER 19 10

**Question 10**

**Why is notebook parameterization using DBUtils widgets important?**

**A. It permanently stores notebook outputs.** ❌ Incorrect

- Widgets collect input.

- They don't store output.

**B. It automatically creates Delta tables.** ❌ Incorrect

- Widgets only provide values.

**C. It allows the same notebook to be reused with different runtime inputs without changing the code.** ✅ Correct

Instead of writing:

Notebook 1\
\
Sales

Notebook 2\
\
HR

Notebook 3\
\
Finance

You write **one notebook**:

Department Widget\
\
↓\
\
Sales\
\
HR\
\
Finance\
\
Marketing

The same code runs for every department.

This is one of the biggest advantages of widgets.

**D. It replaces Spark DataFrames.** ❌ Incorrect

- Widgets and DataFrames serve different purposes.

**E. It enables Photon Acceleration automatically.** ❌ Incorrect

- Photon is unrelated.

------------------------------------------------------------------------

**Memory Trick**

Widgets

↓

One Notebook

↓

Many Inputs

↓

Reusable Code

------------------------------------------------------------------------

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| Parent notebook | Passes parameters, runs the child notebook, and receives the returned result |
| Create a widget | dbutils.widgets.text() |
| Read a widget value | dbutils.widgets.get() |
| Child notebook filter | Department parameter **and** Active Record = 1 |
| Dynamic table naming | Build the table name using the department parameter (for example, dev.branch.dept_sales) |
| Return a value from the child notebook | dbutils.notebook.exit() |
| Run a child notebook | dbutils.notebook.run() |
| Pass parameters | Supply a Python dictionary to dbutils.notebook.run() |
| Job scheduling options | Frequency, widget parameters, notifications, time zone, Cron expressions, and more |
| Why use widgets? | Write one reusable notebook that accepts different runtime inputs without changing the code |

# [README](./../../../README.md)
