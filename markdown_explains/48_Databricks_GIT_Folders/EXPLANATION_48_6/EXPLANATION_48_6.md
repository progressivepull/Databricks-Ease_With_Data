# EXPLANATION 48 6

**Question 6**

**Why are feature branches commonly used when working with Databricks Git Folders?**

**Correct Answer:**\
**B. They allow developers to work independently without affecting the main branch.**

**Why B is Correct**

Typical workflow:

main

├── feature/login

├── feature/orders

├── feature/report

└── feature/ml

Each developer works independently.

After testing:

- Commit

- Push

- Pull Request

- Merge into main

This protects the main branch from unfinished work and is the recommended collaboration pattern.

**Why the other choices are wrong**

Feature branches are not primarily for backups or permissions.

**Memory Tip**

**Feature Branch = Safe Development**

**Individual YouTube Video**

[<u>YouTube video link</u>](https://www.youtube.com/watch?v=W_eFavJIPKw)

**YouTube Search**

https://www.youtube.com/results?search_query=Git+Feature+Branches

# [README](./../../../README.md)
