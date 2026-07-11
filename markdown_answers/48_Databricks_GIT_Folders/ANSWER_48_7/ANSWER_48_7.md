# ANSWER 48 7

**Question 7**

**Why does the lesson recommend saving Databricks notebooks in Source format instead of the default .ipynb format?**

**A. Source format automatically executes notebooks faster.** ❌ Incorrect

- Execution speed is unaffected.

**B. Source format stores notebooks as .py files, making Git diffs, code reviews, and version control easier.** ✅ Correct

Git compares text.

Python source:

print("Hello")

Easy to review.

Notebook JSON:

{

"cells":\[...\]

}

Much harder to review.

Advantages:

- Cleaner Git diffs

- Easier code reviews

- Better merge handling

- Smaller files

**C. Source format converts notebooks into SQL scripts only.** ❌ Incorrect

- Source format preserves notebook language (Python, SQL, Scala, etc.) in source form; it does not convert everything to SQL.

**D. Source format eliminates the need for Git repositories.** ❌ Incorrect

- Git is still required.

**E. Source format enables automatic deployment to production.** ❌ Incorrect

- CI/CD handles deployments.

**Key Concept**

**Source format = Git-friendly notebooks.**

# [README](./../../../README.md)
