# ANSWER 48 6

**Question 6**

**Why are feature branches commonly used when working with Databricks Git Folders?**

**A. They permanently replace the main branch.** ❌ Incorrect

- Feature branches are temporary.

- After merging, they are often deleted.

**B. They allow developers to work independently without affecting the main branch.** ✅ Correct

Typical workflow:

main

│

├── feature/login

│

├── feature/dashboard

│

└── feature/report

Each developer works independently.

After testing:

Merge into **main**.

**C. They automatically deploy code to production.** ❌ Incorrect

- Deployment is handled by CI/CD tools such as Azure Pipelines.

**D. They eliminate the need for commits.** ❌ Incorrect

- Commits are still required.

**E. They prevent pulling updates from the remote repository.** ❌ Incorrect

- Feature branches can still pull changes.

**Key Concept**

**Feature Branch = Safe place to develop.**

# [README](./../../../README.md)
