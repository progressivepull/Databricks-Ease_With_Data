# ANSWER 19 8

**Question 8**

**How are parameters passed from the parent notebook to the child notebook?**

**A. Through SQL variables only** ❌ Incorrect

- SQL variables are unrelated.

**B. Through Spark configuration settings** ❌ Incorrect

- Spark configs are for Spark behavior.

**C. Using a Python dictionary passed to dbutils.notebook.run()** ✅ Correct

Example:

parameters =\
{\
"department":"Sales",\
"year":"2026"\
}

Then:

dbutils.notebook.run(\
"/ETL/Child",\
300,\
parameters\
)

Each dictionary entry becomes a widget value in the child notebook.

**D. Through Azure Active Directory groups** ❌ Incorrect

- Azure AD manages identities.

**E. By storing them in Delta tables** ❌ Incorrect

- Parameters are passed directly.

------------------------------------------------------------------------

**Memory Trick**

Parameters

↓

Dictionary

↓

run()

------------------------------------------------------------------------

# [README](./../../../README.md)
