# EXPLANATION 32 6

**Question 6**

**What happens when a secret is retrieved using dbutils.secrets.get() inside a Databricks notebook?**

**Correct Answer:** **C. Databricks automatically redacts the secret value in notebook output.**

**Explanation**

If a secret value is displayed or printed, Databricks replaces it with:

\[REDACTED\]

This helps prevent accidental exposure in notebook results, although authorized users with appropriate permissions can still access the secret programmatically.

**Why the Correct Answer is Correct**

Automatic redaction protects against accidental disclosure during notebook execution.

**Why the Other Answers Are Wrong**

- The secret is not encrypted only after retrieval.

- It is not written into notebook metadata.

- It is not permanently visible in notebook output.

**YouTube Video**

[YouTube video link](https://www.youtube.com/watch?v=f4SrT3DDdBo)

**Direct YouTube Link**\
<https://www.youtube.com/watch?v=f4SrT3DDdBo>

**YouTube Search**\
https://www.youtube.com/results?search_query=Databricks+secret+redaction

------------------------------------------------------------------------

# [README](./../../../README.md)
