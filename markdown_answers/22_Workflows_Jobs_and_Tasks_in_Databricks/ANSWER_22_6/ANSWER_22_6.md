# ANSWER 22 6

**Question 6**

**How are notebook parameters typically created so that Workflow parameters can populate them?**

**A. Using Spark configuration files** ❌ Incorrect

- Spark configs configure Spark itself.

**B. Using Delta table properties** ❌ Incorrect

- Table properties configure tables.

**C. Using dbutils.widgets** ✅ Correct

Workflow parameter:

Department\
\
↓\
\
Sales

Notebook:

dbutils.widgets.text(\
"department",\
"Sales"\
)

Then:

department =\
dbutils.widgets.get("department")

The Workflow automatically fills the widget.

**D. Using dbutils.fs** ❌ Incorrect

- File system utilities don't create parameters.

**E. Using DESCRIBE HISTORY** ❌ Incorrect

- Displays Delta transaction history.

------------------------------------------------------------------------

**Memory Trick**

Workflow Parameters

↓

Widgets

------------------------------------------------------------------------

# [README](./../../../README.md)
